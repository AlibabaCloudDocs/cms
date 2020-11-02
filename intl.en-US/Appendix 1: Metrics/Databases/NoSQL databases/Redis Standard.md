# Redis Standard

This topic describes the metrics for ApsaraDB for Redis of the standard architecture.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_kvstore**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Average Response Time|μs|StandardAvgRt|userId and instanceId|Average and Maximum|
|Connection Usage|%|StandardConnectionUsage|userId and instanceId|Average and Maximum|
|Cpu Usage|%|StandardCpuUsage|userId and instanceId|Average and Maximum|
|Command Failed Count|count/s|StandardFailedCount|userId and instanceId|Average and Maximum|
|Hit Rate|%|StandardHitRate|userId and instanceId|Average and Maximum|
|Intranet In|KB/s|StandardIntranetIn|userId and instanceId|Average and Maximum|
|Intranet In Ratio|%|StandardIntranetInRatio|userId and instanceId|Average and Maximum|
|Intranet Out|KB/s|StandardIntranetOut|userId and instanceId|Average and Maximum|
|Intranet Out Ratio|%|StandardIntranetOutRatio|userId and instanceId|Average and Maximum|
|Keys Execution Count|count|StandardKeys|userId and instanceId|Average and Maximum|
|Max Response Time|μs|StandardMaxRt|userId and instanceId|Average and Maximum|
|Memory Usage|%|StandardMemoryUsage|userId and instanceId|Average and Maximum|
|QPS Usage|%|StandardQPSUsage|userId and instanceId|Average and Maximum|
|Used Connection|count|StandardUsedConnection|userId and instanceId|Average and Maximum|
|Used Memory|byte|StandardUsedMemory|userId and instanceId|Average and Maximum|
|Used QPS|count|StandardUsedQPS|userId and instanceId|Average and Maximum|

