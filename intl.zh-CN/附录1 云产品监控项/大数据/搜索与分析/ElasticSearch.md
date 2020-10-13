# ElasticSearch

通过本文您可以了解ElasticSearch的监控项。

-   **Namespace**为**acs\_elasticsearch**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|快照状态|无|ClusterAutSnapshotLatestStatus|userId、clusterId|Maximum|
|集群写入QPS|Count/Second|ClusterIndexQPS|userId、clusterId|Average|
|集群查询QPS|Count/Second|ClusterQueryQPS|userId、clusterId|Average|
|集群状态|无|ClusterStatus|userId、clusterId|Value|
|节点CPU使用率|%|LogstashCpuPercent|userId、instanceId、nodeHost|Maximum|
|节点磁盘使用率|%|LogstashNodeDiskUsage|userId、instanceId、nodeHost|Maximum|
|节点内存使用率|%|LogstashNodeHeapMemory|userId、instanceId、nodeHost|Maximum|
|节点1分钟负载|value|LogStashNodeLoad1m|userId、instanceId、nodeHost|Maximum|
|节点CPU使用率|%|NodeCPUUtilization|userId、clusterId、nodeIP|Average|
|节点磁盘使用率|%|NodeDiskUtilization|userId、clusterId、nodeIP|Average|
|节点HeapMemory使用率|%|NodeHeapMemoryUtilization|userId、clusterId、nodeIP|Average|
|节点Load\_1m|无|NodeLoad\_1m|userId、clusterId、nodeIP|Average|
|Exception次数|Count|NodeStatsExceptionLogCount|userId、clusterId、nodeIP|Maximum|
|FullGc次数|Count|NodeStatsFullGcCollectionCount|userId、clusterId、nodeIP|Maximum|

