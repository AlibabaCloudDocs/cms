# TSDB

This topic describes the metrics for Time Series Database \(TSDB\).

-   Set the **Namespace** parameter to **acs\_hitsdb**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Data Points Increment|count|DataPointsIncrement|userId, instanceId, and database|Value|
|DiskUtilization|GB|DiskUtilization|userId and instanceId|Value|
|Total Time Series|count|TotalTimeSeries|userId, instanceId, and database|Value|
|CPU Usage|%|CpuUsage|userId, instanceId, and host|Maximum|
|Memory Usage|%|MemUsage|userId, instanceId, and host|Maximum|

