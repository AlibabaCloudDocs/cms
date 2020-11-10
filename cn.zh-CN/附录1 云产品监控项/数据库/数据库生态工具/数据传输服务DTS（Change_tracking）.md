# 数据传输服务DTS（Change\_tracking）

通过本文您可以了解数据传输服务DTS的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_dts**。
-   **Period**默认为60秒，也可以为60的整数倍。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|订阅延迟|Seconds|ChangeTrackingLatency|userId、instanceId|Average|

