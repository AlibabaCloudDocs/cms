# Redis Cluster

This topic describes the metrics for ApsaraDB for Redis of the cluster architecture.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_kvstore**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Average Response Time|μs|ShardingAvgRt|userId, instanceId, and nodeId|Average and Maximum|
|Connection Usage|%|ShardingConnectionUsage|userId, instanceId, and nodeId|Average and Maximum|
|Cpu Usage|%|ShardingCpuUsage|userId, instanceId, and nodeId|Average and Maximum|
|Hit Rate|%|ShardingHitRate|userId, instanceId, and nodeId|Average and Maximum|
|Intranet In|KB/s|ShardingIntranetIn|userId, instanceId, and nodeId|Average and Maximum|
|Intranet In Ratio|%|ShardingIntranetInRatio|userId, instanceId, and nodeId|Average and Maximum|
|Intranet Out|KB/s|ShardingIntranetOut|userId, instanceId, and nodeId|Average and Maximum|
|Intranet Out Ratio|%|ShardingIntranetOutRatio|userId, instanceId, and nodeId|Average and Maximum|
|Keys Execution Count|count|ShardingKeys|userId, instanceId, and nodeId|Average and Maximum|
|Max Response Time|μs|ShardingMaxRt|userId, instanceId, and nodeId|Average and Maximum|
|Memory Usage|%|ShardingMemoryUsage|userId, instanceId, and nodeId|Average and Maximum|
|QPS Usage|%|ShardingQPSUsage|userId, instanceId, and nodeId|Average and Maximum|
|Used Connection|count|ShardingUsedConnection|userId, instanceId, and nodeId|Average and Maximum|
|Used Memory|byte|ShardingUsedMemory|userId, instanceId, and nodeId|Average, Maximum, and Sum|
|Used QPS|count|ShardingUsedQPS|userId, instanceId, and nodeId|Average and Maximum|

