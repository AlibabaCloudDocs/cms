# ApsaraDB for MongoDB-Cluster Instance

This topic describes the metrics for ApsaraDB for MongoDB of the sharded cluster architecture.

-   Set the **Namespace** parameter to **acs\_mongodb**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|\(Cluster\) CPU Usage|%|ShardingCPUUtilization|userId, instanceId, subinstanceId, and role|Maximum, Minimum, and Average|
|\(Cluster\) Total Connections|count|ShardingConnectionAmount|userId, instanceId, subinstanceId, and role|Maximum, Minimum, and Average|
|\(Cluster\) Connection Usage|%|ShardingconnectionUtilization|userId, instanceId, subinstanceId, and role|Maximum, Minimum, and Average|
|\(Cluster\) Data Disk Usage|byte|ShardingDataDiskAmount|userId, instanceId, subinstanceId, and role|Maximum, Minimum, and Average|
|\(Cluster\) ShardingDataDiskAmountOriginal|N/A|ShardingDataDiskAmountOriginal|userId, instanceId, subinstanceId, and role|Maximum, Minimum, and Average|
|\(Cluster\) Disk Usage|%|ShardingDiskUtilization|userId, instanceId, subinstanceId, and role|Maximum, Minimum, and Average|
|\(Cluster\) IOPS Usage|%|ShardingIOPSUtilization|userId, instanceId, subinstanceId, and role|Maximum, Minimum, and Average|
|\(Cluster\) Instance Disk Usage|byte|ShardingInstanceDiskAmount|userId, instanceId, subinstanceId, and role|Maximum, Minimum, and Average|
|\(Cluster\) Intranet Inbound Traffic|byte|ShardingIntranetIn|userId, instanceId, subinstanceId, and role|Average|
|\(Cluster\) Intranet Outbound Traffic|byte|ShardingIntranetOut|userId, instanceId, subinstanceId, and role|Average|
|\(Cluster\) Log Disk Usage|byte|ShardingLogDiskAmount|userId, instanceId, subinstanceId, and role|Maximum, Minimum, and Average|
|\(Cluster\) Memory Usage|%|ShardingMemoryUtilization|userId, instanceId, subinstanceId, and role|Maximum, Minimum, and Average|
|\(Cluster\) Number of Requests|count|ShardingNumberRequests|userId, instanceId, subinstanceId, and role|Average|
|\(Cluster\) Number of Command Operations|count|ShardingOpCommand|userId, instanceId, subinstanceId, and role|Maximum, Minimum, and Average|
|\(Cluster\) Number of Delete Operations|count|ShardingOpDelete|userId, instanceId, subinstanceId, and role|Maximum, Minimum, and Average|
|\(Cluster\) Number of Getmore Operations|count|ShardingOpGetmore|userId, instanceId, subinstanceId, and role|Maximum, Minimum, and Average|
|\(Cluster\) ShardingOpInsert|count|ShardingOpInsert|userId, instanceId, subinstanceId, and role|Maximum, Minimum, and Average|
|\(Cluster\) Number of Query Operations|count|ShardingOpQuery|userId, instanceId, subinstanceId, and role|Maximum, Minimum, and Average|
|\(Cluster\) Number of Update operations|count|ShardingOpUpdate|userId, instanceId, subinstanceId, and role|Maximum, Minimum, and Average|
|\(Cluster\) QPS|count/s|ShardingQPS|userId, instanceId, subinstanceId, and role|Maximum, Minimum, and Average|

