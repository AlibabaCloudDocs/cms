# 新版云数据库Memcache

通过本文您可以了解新版云数据库Memcache的监控项。

-   **Namespace**为**acs\_memcache**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|连接数使用率|%|ConnectionUsage|userId、instanceId|Maximum、Minimum、Average|
|CPU使用率|%|CpuUsage|userId、instanceId|Maximum、Minimum、Average|
|操作失败数|Count|FailedCount|userId、instanceId|Maximum、Minimum、Average|
|命中率|%|HitRate|userId、instanceId|Maximum、Minimum、Average|
|写入网络带宽|Byte/s|IntranetIn|userId、instanceId|Maximum、Minimum、Average|
|写入带宽使用率|%|IntranetInRatio|userId、instanceId|Maximum、Minimum、Average|
|读取网络带宽|Byte/s|IntranetOut|userId、instanceId|Maximum、Minimum、Average|
|读取带宽使用率|%|IntranetOutRatio|userId、instanceId|Maximum、Minimum、Average|
|内存使用率|%|MemoryUsage|userId、instanceId|Maximum、Minimum、Average|
|已用连接数|Count|UsedConnection|userId、instanceId|Maximum、Minimum、Average|
|内存使用量|Byte|UsedMemory|userId、instanceId|Maximum、Minimum、Average|

