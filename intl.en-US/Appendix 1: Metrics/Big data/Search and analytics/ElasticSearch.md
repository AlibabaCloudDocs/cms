# ElasticSearch

This topic describes the metrics of Elasticsearch.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_elasticsearch**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Node Network out Packages|Count|NodeStatsNetworkoutPackages|userId, clusterId, and nodeIP|Maximum|
|ClusterAutoSnapshotLatestStatus|N/A|ClusterAutoSnapshotLatestStatus|userId and clusterId|Maximum|
|ClusterIndexQPS|Count/Second|ClusterIndexQPS|userId and clusterId|Average|
|ClusterQueryQPS|Count/Second|ClusterQueryQPS|userId and clusterId|Average|
|ClusterStatus|N/A|ClusterStatus|userId and clusterId|Value|
|NodeCPUUtilization|%|NodeCPUUtilization|userId, clusterId, and nodeIP|Average|
|NodeDiskUtilization|%|NodeDiskUtilization|userId, clusterId, and nodeIP|Average|
|NodeHeapMemoryUtilization|%|NodeHeapMemoryUtilization|userId, clusterId, and nodeIP|Average|
|NodeLoad\_1m|N/A|NodeLoad\_1m|userId, clusterId, and nodeIP|Average|
|NodeStatsExceptionLogCount|Count|NodeStatsExceptionLogCount|userId, clusterId, and nodeIP|Maximum|
|NodeStatsFullGcCollectionCount|Count|NodeStatsFullGcCollectionCount|userId, clusterId, and nodeIP|Maximum|

