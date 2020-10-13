# POLARDB MYSQL CLUSTER

This topic describes the metrics for PolarDB for MySQL.

-   Set the **Namespace** parameter to **acs\_polardb**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|ActiveSessions|count|cluster\_active\_sessions|userId, clusterId, and nodeId|Average|
|ConnectionUtilization|%|cluster\_connection\_utilization|userId, clusterId, and nodeId|Average|
|CPUUtilization|%|cluster\_cpu\_utilization|userId, clusterId, and nodeId|Average|
|Input And Output|KB|cluster\_data\_io|userId, clusterId, and nodeId|Average|
|Innodb Input/Output Per Second|count/s|cluster\_data\_iops|userId, clusterId, and nodeId|Average|
|Input/Output Per Second|count/s|cluster\_iops|userId, clusterId, and nodeId|Average|
|Memory Buffer Hit Ratio|%|cluster\_mem\_hit\_ratio|userId, clusterId, and nodeId|Average|
|MemoryUtilization|%|cluster\_memory\_utilization|userId, clusterId, and nodeId|Average|
|QueriesPerSecond|count|cluster\_qps|userId, clusterId, and nodeId|Average|
|Slow Queries Per Second|count/s|cluster\_slow\_queries\_ps|userId, clusterId, and nodeId|Average|
|TransactionsPerSecond|count/s|cluster\_tps|userId, clusterId, and nodeId|Average|

