# Tair容量存储型主从版

通过本文您可以了解Tair容量存储型主从版的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_tair**。
-   **Period**默认为60秒，也可以为60的整数倍。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|RocksDB平均IO时延|us|TairPDBStandardAvgIORt|userId、instanceId|Average、Maximum|
|平均响应时间|us|TairPDBStandardAvgRt|userId、instanceId|Average、Maximum|
|连接数使用率|%|TairPDBStandardConnectionUsage|userId、instanceId|Average、Maximum|
|CPU 使用率|%|TairPDBStandardCpuUsage|userId、instanceId|Average、Maximum|
|磁盘使用率|%|TairPDBStandardDiskUsage|userId、instanceId|Average、Maximum|
|命令失败次数|Count/Second|TairPDBStandardFailedCount|userId、instanceId|Average、Maximum|
|流入带宽|bit/s|TairPDBStandardIntranetIn|userId、instanceId|Average、Maximum|
|流入带宽使用率|%|TairPDBStandardIntranetInRatio|userId、instanceId|Average、Maximum|
|流出带宽|bit/s|TairPDBStandardIntranetOut|userId、instanceId|Average、Maximum|
|流出带宽使用率|%|TairPDBStandardIntranetOutRatio|userId、instanceId|Average、Maximum|
|RocksDB最大IO时延|us|TairPDBStandardMaxIORt|userId、instanceId|Average、Maximum|
|最大响应时间|us|TairPDBStandardMaxRt|userId、instanceId|Average、Maximum|
|内存使用率|%|TairPDBStandardMemoryUsage|userId、instanceId|Average、Maximum|
|QPS使用率|%|TairPDBStandardQPSUsage|userId、instanceId|Average、Maximum|
|命中率|%|TairPDBStandardStandardHitRate|userId、instanceId|Average、Maximum|
|已用连接数|Count|TairPDBStandardUsedConnection|userId、instanceId|Average、Maximum|
|内存使用量|Bytes|TairPDBStandardUsedMemory|userId、instanceId|Average、Maximum|
|平均每秒访问次数|Count|TairPDBStandardUsedQPS|userId、instanceId|Average、Maximum|

