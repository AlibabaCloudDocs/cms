# ApsaraDB for RDS-Disaster Recovery

This topic describes the metrics for the disaster recovery feature of ApsaraDB for RDS.

-   Set the **Namespace** parameter to **acs\_rds\_dashboard**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|Average Data Size of Sync Block|Byte|AvgLogSize|userId, instanceId, and direction|Average|
|Sync Traffic|Byte/s|Flow|userId, instanceId, and direction|Average|
|Max Data Size of Sync Block|Byte|MaxLogSize|userId, instanceId, and direction|Average|
|Sync Delay|ms|Rt|userId, instanceId, and direction|Average|
|Sync Speed|Transactions/Second|TPS|userId, instanceId, and direction|Average|

