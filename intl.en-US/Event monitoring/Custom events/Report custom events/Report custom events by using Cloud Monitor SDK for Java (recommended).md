# Report custom events by using Cloud Monitor SDK for Java \(recommended\)

This topic describes how to report custom events by using Cloud Monitor SDK for Java.

## Install Cloud Monitor SDK for Java

You can install Cloud Monitor SDK for Java by adding the following Maven dependency:

```
<dependency>
            <groupId>com.aliyun.openservices</groupId>
            <artifactId>aliyun-cms</artifactId>
            <version>0.2.4</version>
</dependency>
```

## Sample code

The following sample code shows how to report custom events by using Cloud Monitor SDK for Java:

```
public void uploadEvent() throws CMSException, InterruptedException {
        // Initialize the client.
        CMSClient cmsClient = new CMSClient(endpoint, accKey, secret);
       // Construct two events to be reported.
         CustomEventUploadRequest request = CustomEventUploadRequest.builder()
                    .append(CustomEvent.builder()
                            .setContent("abc,123")
                            .setGroupId(101l)
                            .setName("Event001").build())
                    .append(CustomEvent.builder()
                            .setContent("abc,123")
                            .setGroupId(101l)
                            .setName("Event002").build())
                    .build();
            CustomEventUploadResponse response = cmsClient.putCustomEvent(request);
            List<CustomEvent> eventList = new ArrayList<CustomEvent>();
            eventList.add(CustomEvent.builder()
                    .setContent("abcd,1234")
                    .setGroupId(101l)
                    .setName("Event001").build());
            eventList.add(CustomEvent.builder()
                    .setContent("abcd,1234")
                    .setGroupId(101l)
                    .setName("Event002").build());
            request = CustomEventUploadRequest.builder()
                    .setEventList(eventList).build();
            response = cmsClient.putCustomEvent(request);
    }
```

**Note:** The endpoint is used to access Cloud Monitor. The endpoint is in the format of `metrics.aliyuncs.com`. For more information about Cloud Monitor endpoints in different regions, see [Cloud Monitor endpoints](/intl.en-US/API Reference/Request method.md).

## Sample success responses

The following code shows the sample response that reports custom events by using SDK for Java:

```
{
    "Message": "success",
    "RequestId": "E25EE651-9C97-4EFD-AF22-A753B674E8D4",
    "Code": "200"
}
```

The HTTP status code 200 indicates that the custom events were reported.

