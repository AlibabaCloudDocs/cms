# KVStore for Redis-Disaster Recovery \(Not recommend\)

This topic describes the metrics for the Global Replica feature of ApsaraDB for Redis.

This topic describes the metrics for the Global Replica feature of ApsaraDB for Redis.

-   Set the **Namespace** parameter to **acs\_kvstore**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Average Data Size of Sync Block|byte|AvgLogSize|userId, instanceId, and direction|Average|
|Sync Traffic|byte/s|Flow|userId, instanceId, and direction|Average|
|Max Data Size of Sync Block|byte|MaxLogSize|userId, instanceId, and direction|Average|
|Sync Delay|ms|Rt|userId, instanceId, and direction|Average|
|Sync Speed|transaction/s|TPS|userId, instanceId, and direction|Average|

