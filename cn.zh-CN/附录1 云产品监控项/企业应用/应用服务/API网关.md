# API网关

通过本文您可以了解API网关的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_apigateway\_dashboard**。
-   **Period**默认为60秒，也可以为60的整数倍。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|（旧版）响应时间|ms|Latency|userId、region、apiUid|Average|
|响应时间|ms|Latency\_stage|userId、region、apiUid、apiStageName|Average|
|（旧版）总体请求次数|Count|SumQPS|userId、region、apiUid|Count|
|总体请求次数|Count|SumQPS\_stage|userId、region、apiUid、apiStageName|Count|
|（旧版）流入流量|KBytes|TrafficRX|userId、region、apiUid|Sum|
|流入流量|KBytes|TrafficRX\_stage|userId、region、apiUid、apiStageName|Sum|
|（旧版）流出流量|KBytes|TrafficTX|userId、region、apiUid|Sum|
|流出流量|KBytes|TrafficTX\_stage|userId、region、apiUid、apiStageName|Sum|
|（旧版）返回码2XX个数|Count|code2XX|userId、region、apiUid|Value|
|返回码2XX个数|Count|code2XX\_stage|userId、region、apiUid、apiStageName|Value|
|（旧版）返回码4XX个数|Count|code4XX|userId、region、apiUid|Value|
|返回码4XX个数|Count|code4XX\_stage|userId、region、apiUid、apiStageName|Value|
|（旧版）返回码5XX个数|Count|code5XX|userId、region、apiUid|Value|
|返回码5XX个数|Count|code5XX\_stage|userId、region、apiUid、apiStageName|Value|

