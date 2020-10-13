# AnalyticDB for PostgreSQL

This topic describes the metrics for AnalyticDB for PostgreSQL.

-   Set the **Namespace** parameter to **acs\_hybriddb**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|ConnectionUsage|%|ConnectionUsage|userId, instanceId, and role|Average|
|CpuUsage|%|CpuUsage|userId, instanceId, and role|Average, Maximum, and Minimum|
|DiskUsage|%|DiskUsage|userId, instanceId, and role|Average|
|IOPSUsage|%|IOPSUsage|userId, instanceId, and role|Average|
|MemoryUsage|%|MemoryUsage|userId, instanceId, and role|Average|
|adbpg\_conn\_count|count|adbpg\_conn\_count|userId, instanceId, instance\_component, and hostname|Average, Maximum, and Minimum|
|node\_cpu\_used\_percent|%|node\_cpu\_used\_percent|userId, instanceId, instance\_component, and hostname|Average, Maximum, and Minimum|
|node\_disk\_iops|count|node\_disk\_iops|userId, instanceId, instance\_component, and hostname|Average, Maximum, and Minimum|
|node\_disk\_used\_percent|%|node\_disk\_used\_percent|userId, instanceId, instance\_component, and hostname|Average, Maximum, and Minimum|
|node\_mem\_used\_percent|%|node\_mem\_used\_percent|userId, instanceId, instance\_component, and hostname|Average, Maximum, and Minimum|

