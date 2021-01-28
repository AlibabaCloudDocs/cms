# AnalyticDB for MySQL 3.0

This topic describes the metrics for AnalyticDB for MySQL 3.0.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_adb**.
-   Set the **Period** parameter to an integral multiple of 60. Default value: 60. Unit: seconds.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Connections|count|connections|userId and instanceId|Average|
|DiskUsedPercent|%|disk\_used\_percent|userId and instanceId|Average|
|InsertAvgRt|ms|insert\_avg\_rt|userId and instanceId|Average|
|InsertInBytes|MB|insert\_in\_bytes|userId and instanceId|Average|
|InsertMaxRt|ms|insert\_max\_rt|userId and instanceId|Average|
|QPS|count|qps|userId and instanceId|Average|
|QueryAvgRt|ms|query\_avg\_rt|userId and instanceId|Average|
|QueryMaRt|ms|query\_max\_rt|userId and instanceId|Average|
|QueryTotalWaitTime|ms|query\_total\_wait\_time|userId and instanceId|Average|
|TPS|count|tps|userId and instanceId|Average|
|AvgCpuUsed|%|worker\_avg\_cpu\_used|userId and instanceId|Average|
|AvgReadBytes|MB|worker\_avg\_read\_bytes|userId and instanceId|Average|
|AvgReadIOPS|count/s|worker\_avg\_iops|userId and instanceId|Average|
|AvgWriteBytes|MB|worker\_avg\_bytes|userId and instanceId|Average|
|AvgWriteIOPS|count/s|worker\_avg\_iops|userId and instanceId|Average|

