# 云数据库PolarDB-MySQL（新版）

通过本文您可以了解云数据库PolarDB的MySQL版的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_polardb**。
-   **Period**默认为60秒，也可以为60的整数倍。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

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

**说明：** 每秒慢查询数量的含义和注意事项如下：

-   每秒慢查询数量是分钟秒级平均值，例如：一分钟内产生一条慢SQL，每秒慢查询数量的计算公式：1/60=0.016。
-   由于云数据库RDS需要对实例进行日常维护，也可能产生慢SQL，建议您在使用报警功能时，每秒慢查询数量的阈值不要设置过小，例如：阈值不要设置为0，推荐设置为1。

