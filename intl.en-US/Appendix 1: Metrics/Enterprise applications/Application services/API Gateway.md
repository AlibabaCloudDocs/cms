# API Gateway

This topic describes the metrics for API Gateway.

-   Set the **Namespace** parameter to **acs\_apigateway\_dashboard**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|Latency|ms|Latency|userId, region, and apiUid|Average|
|Overall QPS|Count|SumQPS|userId, region, and apiUid|Count|
|Inbound Traffic|KB|TrafficRX|userId, region, and apiUid|Sum|
|Outbound Traffic|KB|TrafficTX|userId, region, and apiUid|Sum|
|code2XX|Count|code2XX|userId, region, and apiUid|Value|
|code4XX|Count|code4XX|userId, region, and apiUid|Value|
|code5XX|Count|code5XX|userId, region, and apiUid|Value|

