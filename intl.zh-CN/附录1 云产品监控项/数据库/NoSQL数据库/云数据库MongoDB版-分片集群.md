# 云数据库MongoDB版-分片集群

通过本文您可以了解云数据库MongoDB版的分片集群的监控项。

-   **Namespace**为**acs\_mongodb**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|（分片集群）CPU使用率|%|ShardingCPUUtilization|userId、instanceId、subinstanceId、role|Maximum、Minimim、Average|
|（分片集群）连接数量|Count|ShardingConnectionAmount|userId、instanceId、subinstanceId、role|Maximum、Minimim、Average|
|（分片集群）连接使用率|%|ShardingconnectionUtilization|userId、instanceId、subinstanceId、role|Maximum、Minimim、Average|
|（分片集群）数据占用磁盘空间量|Byte|ShardingDataDiskAmount|userId、instanceId、subinstanceId、role|Maximum、Minimim、Average|
|（分片集群）ShardingDataDiskAmountOriginal|无|ShardingDataDiskAmountOriginal|userId、instanceId、subinstanceId、role|Maximum、Minimim、Average|
|（分片集群）磁盘使用率|%|ShardingDiskUtilization|userId、instanceId、subinstanceId、role|Maximum、Minimim、Average|
|（分片集群）IOPS使用率|%|ShardingIOPSUtilization|userId、instanceId、subinstanceId、role|Maximum、Minimim、Average|
|（分片集群）实例占用磁盘空间量|Byte|ShardingInstanceDiskAmount|userId、instanceId、subinstanceId、role|Maximum、Minimim、Average|
|（分片集群）内网入流量|Byte|ShardingIntranetIn|userId、instanceId、subinstanceId、role|Average|
|（分片集群）内网出流量|Byte|ShardingIntranetOut|userId、instanceId、subinstanceId、role|Average|
|（分片集群）日志磁盘使用量|Byte|ShardingLogDiskAmount|userId、instanceId、subinstanceId、role|Maximum、Minimim、Average|
|（分片集群）内存使用率|%|ShardingMemoryUtilization|userId、instanceId、subinstanceId、role|Maximum、Minimum、Average|
|（分片集群）请求数|Count|ShardingNumberRequests|userId、instanceId、subinstanceId、role|Average|
|（分片集群）Command操作次数|Count|ShardingOpCommand|userId、instanceId、subinstanceId、role|Maximum、Minimum、Average|
|（分片集群）Delete操作次数|Count|ShardingOpDelete|userId、instanceId、subinstanceId、role|Maximum、Minimum、Average|
|（分片集群）Getmore操作次数|Count|ShardingOpGetmore|userId、instanceId、subinstanceId、role|Maximum、Minimum、Average|
|（分片集群）ShardingOpInsert|Count|ShardingOpInsert|userId、instanceId、subinstanceId、role|Maximum、Minimum、Average|
|（分片集群）Query操作次数|Count|ShardingOpQuery|userId、instanceId、subinstanceId、role|Maximum、Minimum、Average|
|（分片集群）Update操作次数|Count|ShardingOpUpdate|userId、instanceId、subinstanceId、role|Maximum、Minimum、Average|
|（分片集群）QPS|Count/s|ShardingQPS|userId、instanceId、subinstanceId、role|Maximum、Minimum、Average|

