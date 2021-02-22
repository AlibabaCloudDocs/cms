# \(Recommended\) Report monitoring data by using the SDK for Java

This topic describes how to report monitoring data by using the SDK for Java.

The SDK for Java allows you to report monitoring data by using one of the following methods:

-   Use the SDK for Java to directly report monitoring data.
-   Use the SDK for Java to locally aggregate data and then report the aggregate data.

    The aggregation period must be 60s or 300s.


## Install the SDK for Java

You can install the SDK for Java by adding the following Maven dependency:

```
<dependency>
            <groupId>com.aliyun.openservices</groupId>
            <artifactId>aliyun-cms</artifactId>
            <version>0.2.4</version>
</dependency>
```

## Sample code

The following sample code shows how to report monitoring data by using the SDK for Java:

-   Report raw data

    ```
    CMSClientInit.groupId = 101L;// Specify the ID of the common application group.
            CMSClient cmsClient = new CMSClient(endpoint, accKey, secret);// Initialize the client.
            CustomMetricUploadRequest request = CustomMetricUploadRequest.builder()
                    .append(CustomMetric.builder()
                            .setMetricName("testMetric")// Specify the name of the metric.
                            .setGroupId(102L)// Specify the ID of the application group.
                            .setTime(new Date())
                            .setType(CustomMetric.TYPE_VALUE)// Set the type to raw data.
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
                            .setType(CustomMetric.TYPE_AGG)// Set the type to aggregate data.
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


**Note:** An endpoint is the access address of a cloud service. The endpoints of Cloud Monitor are in the format of `metrics.aliyuncs.com`. For more information about the endpoints of Cloud Monitor in different regions, see [Endpoint](/intl.en-US/Custom monitoring/Report monitoring data/Report monitoring data by sending an HTTP request.md).

## Sample response

The following code shows the sample response that is returned when you report monitoring data by using the SDK for Java:

```
{
    "Message": "success",
    "RequestId": "E25EE651-9C97-4EFD-AF22-A753B674E8D4",
    "Code": "200"
}
```

The HTTP status code 200 indicates a success.

## Report aggregate data of multiple aggregation periods

Use the SDK for Java to locally aggregate data and then report the aggregate data.

|Data type|Description|Aggregated value|Memory usage|
|:--------|:----------|:---------------|:-----------|
|value|The common value type.|All properties except LastValue|About 4 KB|
|gauge|The sample value.|LastValue|4Byte|
|meter|The sum and rate.|Sum and SumPerSecond|50Byte|
|counter|Count|SampleCount|10Byte|
|timer|The computing time.|SampleCount, CountPerSecond, Average, Maximum, Minimum, and P10 to P99|About 4 KB|
|histogram|The distribution.|SampleCount, Average, Maximum, Minimum, and P10 to P99|About 4 KB|

**Note:** The memory usage indicates the memory used by a single time series in a single aggregation period.

Sample code:

```
// Initialize data.
        CMSClientInit.groupId = 0L;
        CMSClient cmsClient = new CMSClient(accKey, secret, endpoint);// Create a client.
        CMSMetricRegistryBuilder builder = new CMSMetricRegistryBuilder();
        builder.setCmsClient(cmsClient);
// Create a registry that is used to report data of two aggregation periods.
final MetricRegistry registry = builder.build();
// Alternatively, create a registry that is used to report data of one aggregation period of 1 minute.
final MetricRegistry registry = builder.build(RecordLevel. _60S);
// Use the value type.
ValueWrapper value = registry.value(MetricName.build("value"));
value.update(6.5);
// Use the meter type.
MeterWrapper meter = registry.meter(MetricName.build("meter"));
meter.update(7.2);
// Use the counter type.
CounterWrapper counter = registry.counter(MetricName.build("counter"));
counter.inc(20);
counter.dec(5);
// Use the timer type.
TimerWrapper timer = registry.timer(MetricName.build("timer"));
timer.update(30, TimeUnit.MILLISECONDS);
// Use the histogram type.
HistogramWrapper histogram = registry.histogram(MetricName.build("histogram"));
histogram.update(20);
// Use the gauge type.
final List list = new ArrayList();
registry.gauge(MetricName.build("gauge"), new Gauge() {
                        @Override
                        public Number getValue() {
                            return list.size();
                        }
                    });
```

