# Stream Computing

This topic describes the metrics for Realtime Compute.

**Note:** Realtime Compute is a stream processing platform provided by Alibaba Cloud.

-   Set the **Namespace** parameter to **acs\_streamcompute**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Fetched Delay|s|FetchedDelay|userId, regionId, projectName, and jobName|Average|
|Read RPS|count/s|ParserTpsRate|userId, regionId, projectName, and jobName|Average|
|Write RPS|count/s|SinkOutTpsRate|userId, regionId, projectName, and jobName|Average|
|FailoverRate|%|TaskFailoverRate|userId, regionId, projectName, and jobName|Average|
|Response Delay|s|inputDelay|userId, regionId, projectName, and jobName|Average|

