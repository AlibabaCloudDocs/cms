# 云数据库POLARDB-MySQL（新版）

通过本文您可以了解云数据库POLARDB的MySQL版的监控项。

-   **Namespace**为**acs\_polardb**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|活跃连接数|Count|cluster\_active\_sessions|userId、clusterId、nodeId|Average|
|连接数使用率|%|cluster\_connection\_utilization|userId、clusterId、nodeId|Average|
|CPU使用率|%|cluster\_cpu\_utilization|userId、clusterId、nodeId|Average|
|每秒存储引擎IO吞吐量|KB|cluster\_data\_io|userId、clusterId、nodeId|Average|
|每秒存储引擎IO次数|CountSecond|cluster\_data\_iops|userId、clusterId、nodeId|Average|
|每秒IO次数|CountSecond|cluster\_iops|userId、clusterId、nodeId|Average|
|内存命中率|%|cluster\_mem\_hit\_ratio|userId、clusterId、nodeId|Average|
|内存使用率|%|cluster\_memory\_utilization|userId、clusterId、nodeId|Average|
|每秒查询数量|Count|cluster\_qps|userId、clusterId、nodeId|Average|
|每秒慢查询数量|CountS|cluster\_slow\_queries\_ps|userId、clusterId、nodeId|Average|
|每秒事务数|CountS|cluster\_tps|userId、clusterId、nodeId|Average|

