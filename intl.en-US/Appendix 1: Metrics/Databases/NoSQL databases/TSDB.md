# TSDB

This topic describes the metrics of Time Series Database \(TSDB\).

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_hitsdb**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|Data Points Increment|Count|DataPointsIncrement|userId, instanceId, and database|Value|
|Disk Utilization|GB|DiskUtilization|userId and instanceId|Value|
|Total Time Series|Count|TotalTimeSeries|userId, instanceId, and database|Value|
|Cpu Usage|%|CpuUsage|userId, instanceId, and host|Maximum|
|Memory Usage|%|MemUsage|userId, instanceId, and host|Maximum|
|TSDB-Memory Usage|%|MemUsage-TSDB|instanceId and host|Maximum|

