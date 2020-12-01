# AnalyticDB for PostgreSQL

This topic describes the metrics of AnalyticDB for PostgreSQL.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_hybriddb**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|ConnectionUsage|%|ConnectionUsage|userId, instanceId, and role|Average|
|CpuUsage|%|CpuUsage|userId, instanceId, and role|Average, Maximum, and Minimum|
|DiskUsage|%|DiskUsage|userId, instanceId, and role|Average|
|IOPSUsage|%|IOPSUsage|userId, instanceId, and role|Average|
|MemoryUsage|%|MemoryUsage|userId, instanceId, and role|Average|
|adbpg\_conn\_count|Count|adbpg\_conn\_count|userId, instanceId, instance\_component, and hostname|Average, Maximum, and Minimum|
|node\_cpu\_used\_percent|%|node\_cpu\_used\_percent|userId, instanceId, instance\_component, and hostname|Average, Maximum, and Minimum|
|node\_disk\_iops|Count|node\_disk\_iops|userId, instanceId, instance\_component, and hostname|Average, Maximum, and Minimum|
|node\_disk\_used\_percent|%|node\_disk\_used\_percent|userId, instanceId, instance\_component, and hostname|Average, Maximum, and Minimum|
|node\_mem\_used\_percent|%|node\_mem\_used\_percent|userId, instanceId, instance\_component, and hostname|Average, Maximum, and Minimum|

