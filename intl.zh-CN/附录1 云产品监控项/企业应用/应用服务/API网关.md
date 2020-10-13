# API网关

通过本文您可以了解API网关的监控项。

-   **Namespace**为**acs\_apigateway\_dashboard**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|响应时间|ms|Latency|userId、region、apiUid|Average|
|总体QPS|Count|SumQPS|userId、region、apiUid|Count|
|流入带宽|KB|TrafficRX|userId、region、apiUid|Sum|
|流出带宽|KB|TrafficTX|userId、region、apiUid|Sum|
|code2XX|Count|code2XX|userId、region、apiUid|Value|
|code4XX|Count|code4XX|userId、region、apiUid|Value|
|code5XX|Count|code5XX|userId、region、apiUid|Value|

