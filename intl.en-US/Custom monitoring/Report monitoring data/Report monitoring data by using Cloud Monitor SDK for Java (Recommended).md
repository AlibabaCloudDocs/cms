# Report monitoring data by using Cloud Monitor SDK for Java \(Recommended\)

This topic describes how to report monitoring data by using Cloud Monitor SDK for Java.

Cloud Monitor SDK for Java allows you to report monitoring data by using one of the following methods:

-   Use Cloud Monitor SDK for Java to report raw data to Cloud Monitor.
-   Use Cloud Monitor SDK for Java to aggregate data on a local host and then report the aggregate data to Cloud Monitor.

    The aggregation period must be 60s or 300s.


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

The following sample code shows how to report monitoring data by using Cloud Monitor SDK for Java:

-   Report raw data

    ```
    CMSClientInit.groupId = 101L;// Specify the ID of the common application group.
            CMSClient cmsClient = new CMSClient(endpoint, accKey, secret);// Initialize the client.
            CustomMetricUploadRequest request = CustomMetricUploadRequest.builder()
                    .append(CustomMetric.builder()
                            .setMetricName("testMetric")// Specify the name of the metric.
                            .setGroupId(102L)// Specify the ID of the application group.
                            .setTime(new Date())
                            .setType(CustomMetric.TYPE_VALUE)// Specify the type of the data to be reported. In this example, raw data is reported.
                            .appendValue(MetricAttribute.VALUE, 1f)// Add raw data. Set the key to MetricAttribute.VALUE.
                            .appendDimension("key", "value")// Add a dimension.
                            .appendDimension("ip", "127.0.0.1")// Add a dimension.
                            .build())
                    .build();
            CustomMetricUploadResponse response = cmsClient.putCustomMetric(request);// Report data.
            System.out.println(JSONObject.toJSONString(response));
    ```

-   Report aggregate data

    ```
    CMSClientInit.groupId = 101L;
            CMSClient cmsClient = new CMSClient(endpoint, accKey, secret);
            CustomMetricUploadRequest request = CustomMetricUploadRequest.builder()
                    .append(CustomMetric.builder()
                            .setMetricName("customTest")
                            .setTime(new Date())
                            .setType(CustomMetric.TYPE_AGG)// Specify the type of the data to be reported. In this example, aggregate data is reported.
                            .setPeriod(CustomMetric.PERIOD_1M)// Set the aggregation period to 1 minute.
                            .appendDimension("test", "testValue")// Add a dimension.
                            .appendDimension("dimension", "dimensionValue")// Add a dimension.
                            .appendValue(MetricAttribute.SUM, 100)// Add the total value.
                            .appendValue(MetricAttribute.MAX, 20)// Add the maximum value.
                            .appendValue(MetricAttribute.MIN, 0.1)// Add the minimum value.
                            .appendValue(MetricAttribute.COUNT, 20)// Add the count.
                            .appendValue(MetricAttribute.AVG, 5)// Add the average value.
                            .appendValue(MetricAttribute.LAST, 10)// Add the last sample value of the aggregation period.
                            .appendValue(MetricAttribute.P50, 10)// Add the value of the 50th percentile.
                            .appendValue(MetricAttribute.P90, 17)// Add the value of the 90th percentile.
                            .appendValue(MetricAttribute.P99, 19)// Add the value of the 99th percentile.
                            .build())
                    .build();
            CustomMetricUploadResponse response = cmsClient.putCustomMetric(request);
            System.out.println(JSONObject.toJSONString(response));
    ```


## Sample success response

The following code shows the sample response for reporting monitoring data by using Cloud Monitor SDK for Java:

```
{
    "Message": "success",
    "RequestId": "E25EE651-9C97-4EFD-AF22-A753B674E8D4",
    "Code": "200"
}
```

The HTTP status code 200 indicates that the monitoring data was reported.

## Report aggregate data of multiple aggregation periods

You can use Cloud Monitor SDK for Java to aggregate data on a local host and report the aggregate data to Cloud Monitor.

|Date type|Description|Aggregated value|Memory usage|
|:--------|:----------|:---------------|:-----------|
|value|The common value type.|All values except LastValue|About 4 KB|
|gauge|The sample value.|LastValue|4 bytes|
|meter|The total value and the total value divided by the total number of seconds of the aggregation period.|Sum and SumPerSecond|50 bytes|
|counter|The count of sample values.|SampleCount|10 bytes|
|timer|The data related to time.|SampleCount, CountPerSecond, Average, Maximum, Minimum, and PXX \(P10 to P99\)|About 4 KB|
|histogram|The distribution of values.|SampleCount, Average, Maximum, Minimum, and PXX \(P10 to P99\)|About 4 KB|

**Note:** The memory usage indicates the memory used by aggregate data of a single time series metric in a single aggregation period.

Sample code:

```
// Initialize related data.
        CMSClientInit.groupId = 0L;
        CMSClient cmsClient = new CMSClient(accKey, secret, endpoint);// Create a client.
        CMSMetricRegistryBuilder builder = new CMSMetricRegistryBuilder();
        builder.setCmsClient(cmsClient);
// Create a registry that is used to report data of two aggregation periods.
final MetricRegistry registry = builder.build();
// Alternatively, create a registry that is used to report data of one aggregation period of 1 minute.
final MetricRegistry registry = builder.build(RecordLevel. _60S);
// Generate data of the value type.
ValueWrapper value = registry.value(MetricName.build("value"));
value.update(6.5);
// Generate data of the meter type.
MeterWrapper meter = registry.meter(MetricName.build("meter"));
meter.update(7.2);
// Generate data of the counter type.
CounterWrapper counter = registry.counter(MetricName.build("counter"));
counter.inc(20);
counter.dec(5);
// Generate data of the timer type.
TimerWrapper timer = registry.timer(MetricName.build("timer"));
timer.update(30, TimeUnit.MILLISECONDS);
// Generate data of the histogram type.
HistogramWrapper histogram = registry.histogram(MetricName.build("histogram"));
histogram.update(20);
// Generate data of the gauge type.
final List list = new ArrayList();
registry.gauge(MetricName.build("gauge"), new Gauge() {
                        @Override
                        public Number getValue() {
                            return list.size();
                        }
                    });
```

