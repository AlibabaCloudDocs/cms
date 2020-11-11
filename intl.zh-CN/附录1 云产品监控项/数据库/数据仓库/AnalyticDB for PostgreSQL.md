# AnalyticDB for PostgreSQL

通过本文您可以了解分析型数据库PostgreSQL版的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_hybriddb**。
-   **Period**默认为60秒，也可以为60的整数倍。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|【资源预留】连接数使用率|%|ConnectionUsage|userId、instanceId、role|Average|
|【资源预留】CPU使用率|%|CpuUsage|userId、instanceId、role|Average、Maximum、Minimum|
|【资源预留】磁盘使用率|%|DiskUsage|userId、instanceId、role|Average|
|【资源预留】IO吞吐量使用率|%|IOPSUsage|userId、instanceId、role|Average|
|【资源预留】内存使用率|%|MemoryUsage|userId、instanceId、role|Average|
|【资源弹性】连接数|Count|adbpg\_conn\_count|userId、instanceId、instance\_component、hostname|Average、Maximum、Minimum|
|【资源弹性】节点CPU使用率|%|node\_cpu\_used\_percent|userId、instanceId、instance\_component、hostname|Average、Maximum、Minimum|
|【资源弹性】节点IOPS|Count|node\_disk\_iops|userId、instanceId、instance\_component、hostname|Average、Maximum、Minimum|
|【资源弹性】节点磁盘使用率|%|node\_disk\_used\_percent|userId、instanceId、instance\_component、hostname|Average、Maximum、Minimum|
|【资源弹性】节点内存使用率|%|node\_mem\_used\_percent|userId、instanceId、instance\_component、hostname|Average、Maximum、Minimum|

