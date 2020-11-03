# 通过Java SDK上报监控数据（推荐）

本文为您介绍通过Java SDK上报监控数据的配置方法。

通过Java SDK上报监控数据的方法如下：

-   您可以直接通过Java SDK上报监控数据。
-   您可以先在本地通过Java SDK聚合数据，再通过Java SDK上报监控数据。

    聚合周期为60秒或300秒。


## 安装Java SDK

通过Maven安装Java SDK，需要添加的依赖如下：

```
<dependency>
            <groupId>com.aliyun.openservices</groupId>
            <artifactId>aliyun-cms</artifactId>
            <version>0.2.4</version>
</dependency>
```

## 代码示例

通过Java SDK方式上报监控数据的代码示例如下：

-   上报原始数据

    ```
    CMSClientInit.groupId = 101L;//设置公共的应用分组ID。
            CMSClient cmsClient = new CMSClient(endpoint, accKey, secret);//初始化client。
            CustomMetricUploadRequest request = CustomMetricUploadRequest.builder()
                    .append(CustomMetric.builder()
                            .setMetricName("testMetric")//指标名称。
                            .setGroupId(102L)//设置应用分组ID。
                            .setTime(new Date())
                            .setType(CustomMetric.TYPE_VALUE)//类型为原始值。
                            .appendValue(MetricAttribute.VALUE, 1f)//原始值，key只能是该value，不能自定义。
                            .appendDimension("key", "value")//添加维度。
                            .appendDimension("ip", "127.0.0.1")//添加维度。
                            .build())
                    .build();
            CustomMetricUploadResponse response = cmsClient.putCustomMetric(request);//上报数据。
            System.out.println(JSONObject.toJSONString(response));
    ```

-   上报聚合数据

    ```
    CMSClientInit.groupId = 101L;
            CMSClient cmsClient = new CMSClient(endpoint, accKey, secret);
            CustomMetricUploadRequest request = CustomMetricUploadRequest.builder()
                    .append(CustomMetric.builder()
                            .setMetricName("customTest")
                            .setTime(new Date())
                            .setType(CustomMetric.TYPE_AGG)//类型为聚合。
                            .setPeriod(CustomMetric.PERIOD_1M)//周期为1分钟。
                            .appendDimension("test", "testValue")//设置维度。
                            .appendDimension("dimension", "dimensionValue")//设置维度。
                            .appendValue(MetricAttribute.SUM, 100)//设置求和。
                            .appendValue(MetricAttribute.MAX, 20)//设置最大值。
                            .appendValue(MetricAttribute.MIN, 0.1)//设置最小值。
                            .appendValue(MetricAttribute.COUNT, 20)//设置计数。
                            .appendValue(MetricAttribute.AVG, 5)//设置平均值。
                            .appendValue(MetricAttribute.LAST, 10)//设置周期最后一个值。
                            .appendValue(MetricAttribute.P50, 10)//设置P50。
                            .appendValue(MetricAttribute.P90, 17)//设置P90。
                            .appendValue(MetricAttribute.P99, 19)//设置P99。
                            .build())
                    .build();
            CustomMetricUploadResponse response = cmsClient.putCustomMetric(request);
            System.out.println(JSONObject.toJSONString(response));
    ```


**说明：** endpoint是云服务的接入地址，云监控的接入地址为`metrics.aliyuncs.com`。云监控各地域的接入地址，请参见[云监控接入地址](/intl.zh-CN/API参考/调用API.md)。

## 返回示例

通过Java SDK方式上报监控数据的代码返回示例如下：

```
{
    "Message": "success",
    "RequestId": "E25EE651-9C97-4EFD-AF22-A753B674E8D4",
    "Code": "200"
}
```

HTTP状态码返回200表示成功。

## 多周期聚合上报

Java SDK支持在本地先聚合数据，再上报监控数据的功能。

|数据类型|描述|聚合的值|内存消耗|
|:---|:-|:---|:---|
|value|一般值类型|除了LastValue外的所有属性|约4KB|
|gauge|采样值|LastValue|4Byte|
|meter|求和、速率|Sum、SumPerSecond|50Byte|
|counter|计数|SampleCount|10Byte|
|timer|计算时间|SampleCount、CountPerSecond、Average、Maximum、Minimum、PXX（P10-P99）|约4KB|
|histogram|分布|SampleCount、Average、Maximum、Minimum、PXX（P10-P99）|约4KB|

**说明：** 内存消耗是单时间序列和单聚合周期。

代码示例如下：

```
//初始化
        CMSClientInit.groupId = 0L;
        CMSClient cmsClient = new CMSClient(accKey, secret, endpoint);//创建client。
        CMSMetricRegistryBuilder builder = new CMSMetricRegistryBuilder();
        builder.setCmsClient(cmsClient);
//创建registry，包含2个聚合周期。
final MetricRegistry registry = builder.build();
//或创建registry，只创建1分钟聚合周期。
final MetricRegistry registry = builder.build(RecordLevel._60S);
//使用value。
ValueWrapper value = registry.value(MetricName.build("value"));
value.update(6.5);
//使用meter。
MeterWrapper meter = registry.meter(MetricName.build("meter"));
meter.update(7.2);
//使用counter。
CounterWrapper counter = registry.counter(MetricName.build("counter"));
counter.inc(20);
counter.dec(5);
//使用timer。
TimerWrapper timer = registry.timer(MetricName.build("timer"));
timer.update(30, TimeUnit.MILLISECONDS);
//使用histogram。
HistogramWrapper histogram = registry.histogram(MetricName.build("histogram"));
histogram.update(20);
//使用gauge。
final List list = new ArrayList();
registry.gauge(MetricName.build("gauge"), new Gauge() {
                        @Override
                        public Number getValue() {
                            return list.size();
                        }
                    });
```

