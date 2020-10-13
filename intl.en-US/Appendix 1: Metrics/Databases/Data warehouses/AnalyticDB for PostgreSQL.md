# AnalyticDB for PostgreSQL

This topic describes the metrics for AnalyticDB for PostgreSQL.

-   Set the **Namespace** parameter to **acs\_ads**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|QuotaDiskSpace|MB|ads.diskSize|userId, instanceId, tableSchema, and workerId|Maximum, Minimum, and Average|
|UsedDiskSpace|MB|ads.diskUsed|userId, instanceId, tableSchema, and workerId|Maximum, Minimum, and Average|
|DiskUtilization|%|ads.diskUsedPercent|userId, instanceId, tableSchema, and workerId|Maximum, Minimum, and Average|

