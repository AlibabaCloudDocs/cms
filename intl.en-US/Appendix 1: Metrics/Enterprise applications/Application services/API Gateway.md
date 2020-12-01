# API Gateway

This topic describes the metrics of API Gateway.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_apigateway\_dashboard**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|\(Old\) Latency|ms|Latency|userId, region, and apiUid|Average|
|Latency|ms|Latency\_stage|userId, region, apiUid, and apiStageName|Average|
|\(Old\) SumQPS|Count|SumQPS|userId, region, and apiUid|Count|
|SumQPS|Count|SumQPS\_stage|userId, region, apiUid, and apiStageName|Count|
|\(Old\) TrafficRX|KBytes|TrafficRX|userId, region, and apiUid|Sum|
|TrafficRX|KBytes|TrafficRX\_stage|userId, region, apiUid, and apiStageName|Sum|
|\(Old\) TrafficTX|KBytes|TrafficTX|userId, region, and apiUid|Sum|
|TrafficTX|KBytes|TrafficTX\_stage|userId, region, apiUid, and apiStageName|Sum|
|\(Old\) code2XX Number|Count|code2XX|userId, region, and apiUid|Value|
|code2XX Number|Count|code2XX\_stage|userId, region, apiUid, and apiStageName|Value|
|\(Old\) code4XX Number|Count|code4XX|userId, region, and apiUid|Value|
|code4XX Number|Count|code4XX\_stage|userId, region, apiUid, and apiStageName|Value|
|\(Old\) code5XX Number|Count|code5XX|userId, region, and apiUid|Value|
|code5XX Number|Count|code5XX\_stage|userId, region, apiUid, and apiStageName|Value|

