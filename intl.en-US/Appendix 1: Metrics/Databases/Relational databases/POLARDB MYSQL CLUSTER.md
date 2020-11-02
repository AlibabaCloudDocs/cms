# POLARDB MYSQL CLUSTER

This topic describes the metrics for PolarDB for MySQL.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_polardb**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

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

**Note:** The following information describes how the Slow Queries Per Second metric is measured and the precautions when you set the threshold for this metric:

-   The value of the Slow Queries Per Second metric is the number of slow SQL queries within a minute divided by 60s. For example, if a slow SQL query occurred within a minute, the value of the Slow Queries Per Second metric is calculated by using the following formula: 1/60 = 0.016.
-   During the routine maintenance for ApsaraDB RDS instances, slow SQL queries may occur. Therefore, we recommend that you do not set the threshold of the Slow Queries Per Second metric to a value that is too small, for example, 0. Instead, you can set the threshold to 1.

