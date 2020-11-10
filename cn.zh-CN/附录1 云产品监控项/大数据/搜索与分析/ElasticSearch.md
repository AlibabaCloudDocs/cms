# ElasticSearch

通过本文您可以了解ElasticSearch的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_elasticsearch**。
-   **Period**默认为60秒，也可以为60的整数倍。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|节点网络流出包|Count|NodeStatsNetworkoutPackages|userId、clusterId、nodeIP|Maximum|
|快照状态|无|ClusterAutoSnapshotLatestStatus|userId、clusterId|Maximum|
|集群写入QPS|Count/Second|ClusterIndexQPS|userId、clusterId|Average|
|集群查询QPS|Count/Second|ClusterQueryQPS|userId、clusterId|Average|
|集群状态|无|ClusterStatus|userId、clusterId|Value|
|节点CPU使用率|%|NodeCPUUtilization|userId、clusterId、nodeIP|Average|
|节点磁盘使用率|%|NodeDiskUtilization|userId、clusterId、nodeIP|Average|
|节点HeapMemory使用率|%|NodeHeapMemoryUtilization|userId、clusterId、nodeIP|Average|
|节点Load\_1m|无|NodeLoad\_1m|userId、clusterId、nodeIP|Average|
|Exception次数|Count|NodeStatsExceptionLogCount|userId、clusterId、nodeIP|Maximum|
|FullGc次数|Count|NodeStatsFullGcCollectionCount|userId、clusterId、nodeIP|Maximum|

