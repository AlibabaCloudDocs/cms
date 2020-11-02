# Redis Read-Write

This topic describes the metrics for ApsaraDB for Redis of the read/write splitting architecture.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_kvstore**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Average Response Time|μs|SplitrwAvgRt|userId, instanceId, and nodeId|Average and Maximum|
|Connection Usage|%|SplitrwConnectionUsage|userId, instanceId, and nodeId|Average and Maximum|
|Cpu Usage|%|SplitrwCpuUsage|userId, instanceId, and nodeId|Average and Maximum|
|Command Failed Count|count/s|SplitrwFailedCount|userId, instanceId, and nodeId|Average and Maximum|
|Hit Rate|%|SplitrwHitRate|userId, instanceId, and nodeId|Average and Maximum|
|Intranet In|KB/s|SplitrwIntranetIn|userId, instanceId, and nodeId|Average and Maximum|
|Intranet In Ratio|%|SplitrwIntranetInRatio|userId, instanceId, and nodeId|Average and Maximum|
|Intranet Out|KB/s|SplitrwIntranetOut|userId, instanceId, and nodeId|Average and Maximum|
|Intranet Out Ratio|%|SplitrwIntranetOutRatio|userId, instanceId, and nodeId|Average and Maximum|
|Keys Execution Count|count|SplitrwKeys|userId, instanceId, and nodeId|Average and Maximum|
|Max Response Time|μs|SplitrwMaxRt|userId, instanceId, and nodeId|Average and Maximum|
|Memory Usage|%|SplitrwMemoryUsage|userId, instanceId, and nodeId|Average and Maximum|
|QPS Usage|%|SplitrwQPSUsage|userId, instanceId, and nodeId|Average and Maximum|
|Used Connection|count|SplitrwUsedConnection|userId, instanceId, and nodeId|Average and Maximum|
|Used Memory|byte|SplitrwUsedMemory|userId, instanceId, and nodeId|Average, Maximum, and Sum|
|Used QPS|count|SplitrwUsedQPS|userId, instanceId, and nodeId|Average and Maximum|

