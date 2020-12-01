# ApsaraDB for MongoDB-Cluster Instance

This topic describes the metrics of ApsaraDB for MongoDB of the sharded cluster architecture.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_mongodb**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|\(Cluster\) Number of Command Operations|Count|ShardingOpCommand|userId, instanceId, subinstanceId, and role|Average, Maximum, and Minimum|
|\(Cluster\) Number of Delete Operations|Count|ShardingOpDelete|userId, instanceId, subinstanceId, and role|Average, Maximum, and Minimum|
|\(Cluster\) Log Disk Usage|Bytes|ShardingLogDiskAmount|userId, instanceId, subinstanceId, and role|Average, Maximum, and Minimum|
|\(Cluster\) Memory Usage|%|ShardingMemoryUtilization|userId, instanceId, subinstanceId, and role|Average, Maximum, and Minimum|
|\(Cluster\) Number of Requests|Count|ShardingNumberRequests|userId, instanceId, subinstanceId, and role|Average|
|\(Cluster\) IOPS Usage|%|ShardingIOPSUtilization|userId, instanceId, subinstanceId, and role|Average, Maximum, and Minimum|
|\(Cluster\) Intranet Inbound Traffic|Bytes|ShardingIntranetIn|userId, instanceId, subinstanceId, and role|Average|
|\(Cluster\) Intranet Outbound Traffic|Bytes|ShardingIntranetOut|userId, instanceId, subinstanceId, and role|Average|
|\(Cluster\) Data Disk Usage|Bytes|ShardingDataDiskAmount|userId, instanceId, subinstanceId, and role|Average, Maximum, and Minimum|
|\(Cluster\) CPU Usage|%|ShardingCPUUtilization|userId, instanceId, subinstanceId, and role|Average, Maximum, and Minimum|
|\(Cluster\) Total Connections|Count|ShardingConnectionAmount|userId, instanceId, subinstanceId, and role|Average, Maximum, and Minimum|
|\(Cluster\) Connection Usage|%|ShardingConnectionUtilization|userId, instanceId, subinstanceId, and role|Average, Maximum, and Minimum|
|\(Cluster\) Instance Disk Usage|Bytes|ShardingInstanceDiskAmount|userId, instanceId, subinstanceId, and role|Average, Maximum, and Minimum|
|\(Cluster\) Disk Usage|%|ShardingDiskUtilization|userId, instanceId, subinstanceId, and role|Average, Maximum, and Minimum|
|\(Cluster\) Number of Getmore Operations|Count|ShardingOpGetmore|userId, instanceId, subinstanceId, and role|Average, Maximum, and Minimum|
|\(Cluster\) ShardingOpInsert|Count|ShardingOpInsert|userId, instanceId, subinstanceId, and role|Average, Maximum, and Minimum|
|\(Cluster\) Number of Query Operations|Count|ShardingOpQuery|userId, instanceId, subinstanceId, and role|Average, Maximum, and Minimum|
|\(Cluster\) Number of Update operations|Count|ShardingOpUpdate|userId, instanceId, subinstanceId, and role|Average, Maximum, and Minimum|
|\(Cluster\) QPS|Count/s|ShardingQPS|userId, instanceId, subinstanceId, and role|Average, Maximum, and Minimum|
|\(Cluster\) ShardingDataDiskAmountOriginal|N/A|ShardingDataDiskAmountOriginal|userId, instanceId, subinstanceId, and role|Average, Maximum, and Minimum|

