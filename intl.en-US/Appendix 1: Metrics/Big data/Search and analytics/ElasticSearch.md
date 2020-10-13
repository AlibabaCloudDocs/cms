# ElasticSearch

This topic describes the metrics for Alibaba Cloud Elasticsearch.

-   Set the **Namespace** parameter to **acs\_elasticsearch**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|ClusterAutoSnapshotLatestStatus|N/A|ClusterAutSnapshotLatestStatus|userId and clusterId|Maximum|
|ClusterIndexQPS|count/s|ClusterIndexQPS|userId and clusterId|Average|
|ClusterQueryQPS|count/s|ClusterQueryQPS|userId and clusterId|Average|
|ClusterStatus|N/A|ClusterStatus|userId and clusterId|Value|
|NodeCPUUtilization|%|LogstashCpuPercent|userId, instanceId, and nodeHost|Maximum|
|NodeDiskUtilization|%|LogstashNodeDiskUsage|userId, instanceId, and nodeHost|Maximum|
|NodeHeapMemoryUtilization|%|LogstashNodeHeapMemory|userId, instanceId, and nodeHost|Maximum|
|NodeLoad\_1m|value|LogStashNodeLoad1m|userId, instanceId, and nodeHost|Maximum|
|NodeCPUUtilization|%|NodeCPUUtilization|userId, clusterId, and nodeIP|Average|
|NodeDiskUtilization|%|NodeDiskUtilization|userId, clusterId, and nodeIP|Average|
|NodeHeapMemoryUtilization|%|NodeHeapMemoryUtilization|userId, clusterId, and nodeIP|Average|
|NodeLoad\_1m|N/A|NodeLoad\_1m|userId, clusterId, and nodeIP|Average|
|NodeStatsExceptionLogCount|count|NodeStatsExceptionLogCount|userId, clusterId, and nodeIP|Maximum|
|NodeStatsFullGcCollectionCount|count|NodeStatsFullGcCollectionCount|userId, clusterId, and nodeIP|Maximum|

