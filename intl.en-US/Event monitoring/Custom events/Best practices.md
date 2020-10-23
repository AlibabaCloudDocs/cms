# Best practices

This topic describes how to use the custom event monitoring feature in Cloud Monitor to monitor service exceptions and generate alerts when specific conditions are met.

## Background information

Services may encounter exceptions from time to time. Serious exceptions may even interrupt your business. Only specific exceptions can be automatically resolved with methods such as retries. Most exceptions must be manually handled. Therefore, you require a system to monitor service exceptions and generate alerts when specific conditions are met. The traditional solution is generating logs and collecting them to a specified system such as ELK, which is the acronym for three open source projects: Elasticsearch, Logstash, and Kibana. An open source system often consists of multiple complex and distributed systems. This causes high technical requirements and high costs. Against this background, Cloud Monitor provides the custom event monitoring feature, which allows you to monitor service exceptions with ease.

## Before you begin

The custom event monitoring feature allows you to report custom events by using Cloud Monitor SDK for Java or Cloud Monitor API. In the following example, Cloud Monitor SDK for Java is used to describe how to report custom events.

1.  Install Cloud Monitor SDK for Java by adding the following Maven dependency:

    ```
    <dependency>
        <groupId>com.aliyun.openservices</groupId>
        <artifactId>aliyun-cms</artifactId>
        <version>0.1.2</version>
    </dependency>
    ```

2.  Initialize Cloud Monitor SDK for Java.

    ```
    // The ID of the application group. This parameter is used to classify events by application group. You can query the ID of the application group on the Application Groups page in the Cloud Monitor console.
    CMSClientInit.groupId = 118L;
    // The endpoint for reporting events. A public endpoint is used in this example. The accesskey and secretkey parameters are used for authentication.
    CMSClient c = new CMSClient("https://metrichub-cms-cn-hangzhou.aliyuncs.com", accesskey, secretkey);
    ```

3.  Specify whether to report events asynchronously.

    By default, Cloud Monitor allows you to report events synchronously. The synchronous reporting mode has many advantages. For example, its code is easy to write, and it ensures that all events are reported to Cloud Monitor.

    However, this mode also has drawbacks. To implement synchronous reporting, you must embed the code for reporting events in the business code. If the network conditions between your system and Cloud Monitor degrade, the code for reporting events may fail to be run, which affects the normal running of your business. In addition, you may not require the system to report all events to Cloud Monitor in specific scenarios. To avoid these drawbacks, you can use asynchronous reporting by writing events to an event queue of the LinkedBlockingQueue type. Then, you can use an executor of the ScheduledExecutorService type to asynchronously report multiple events in the event queue at a time.

    ```
    // Initialize the event queue and executor.
    private LinkedBlockingQueue<EventEntry> eventQueue = new LinkedBlockingQueue<EventEntry>(10000);
    private ScheduledExecutorService schedule = Executors.newSingleThreadScheduledExecutor();
    // Add an event to the event queue.
    // An event consists of the name and content. The name identifies the event, and the content provides the event details. Full event content can be searched.
    public void put(String name, String content) {
        EventEntry event = new EventEntry(name, content);
        // The following code discards new events when the event queue is full. You can modify the policy as required.
        boolean b = eventQueue.offer(event);
        if (! b) {
            logger.warn("The following event is discarded because the event queue is full: {}", event);
        }
    }
    // Report events asynchronously. Initialize a scheduled task to call the run method every second. You can change the interval as required.
    schedule.scheduleAtFixedRate(this, 1, 1, TimeUnit.SECONDS);
    public void run() {
        do {
            batchPut();
        } while (this.eventQueue.size() > 500);
    }
    private void batchPut() {
        // Obtain 99 events from the event queue to report them at a time.
        List<CustomEvent> events = new ArrayList<CustomEvent>();
        for (int i = 0; i < 99; i++) {
            EventEntry e = this.eventQueue.poll();
            if (e == null) {
                break;
            }
            events.add(CustomEvent.builder().setContent(e.getContent()).setName(e.getName()).build());
        }
        if (events.isEmpty()) {
            return;
        }
        // Report multiple events to Cloud Monitor at a time. In the following code, event reporting is not retried if an exception occurs. You can add a retry policy if you need to ensure high reliability of event reporting.
        try {
            CustomEventUploadRequestBuilder builder = CustomEventUploadRequest.builder();
            builder.setEventList(events);
            CustomEventUploadResponse response = cmsClient.putCustomEvent(builder.build());
            if (!" 200".equals(response.getErrorCode())) {
                logger.warn("An error occurs during event reporting: msg: {}, rid: {}", response.getErrorMsg(), response.getRequestId());
            }
        } catch (Exception e1) {
            logger.error("An exception occurs during event reporting", e1);
        }
    }
    ```


## Examples of using the custom event monitoring feature

-   Example 1: Monitor HTTP controller exceptions

    The following sample code monitors HTTP requests to detect abnormal HTTP requests. An alert is generated if the number of abnormal HTTP requests in a minute exceeds the specified threshold.

    Cloud Monitor intercepts HTTP requests by using Spring Interceptor or Servlet Filter, records abnormal HTTP requests in logs, and generates alerts based on an alert rule.

    Sample code:

    ```
    // Each event must contain abundant information to help search for and troubleshoot issues. The sample code uses a map to store event information and converts the map to a JSON string as the event content. 
    Map<String, String> eventContent = new HashMap<String, String>();
    eventContent.put("method", "GET"); // The HTTP request method.
    eventContent.put("path", "/users"); // The HTTP path.
    eventContent.put("exception", e.getClass().getName()); // The exception class name, which is used for search.
    eventContent.put("error", e.getMessage()); // The error message.
    eventContent.put("stack_trace", ExceptionUtils.getStackTrace(e)); // The exception stack trace, which is used for troubleshooting.
    // Use the preceding asynchronous reporting method to report events. No retry policy is configured in this method. Events may be lost at a low probability. However, this method can meet requirements for detecting unknown HTTP exceptions.
    put("http_error", JsonUtils.toJson(eventContent));
    ![ image.png](http://ata2-img.cn-hangzhou.img-pub.aliyun-inc.com/864cf095977cf61bd340dd1461a0247c.png)
    ```

-   Example 2: Record key events

    You can also use the custom event monitoring feature to record key events for which alerts do not need to be generated. This allows you to check these events in the future. For example, you can record key business operations, password changes, order changes, and unusual logons.

    ![View key events](../images/p4906.png)


