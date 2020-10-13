# 云数据库Redis版（不推荐）

通过本文您可以了解云数据库Redis版的监控项。

-   **Namespace**为**acs\_kvstore**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|连接数使用率|%|ConnectionUsage|userId、instanceId|Maximum、Minimim、Average|
|CPU使用率|%|CpuUsage|userId、instanceId|Maximum、Minimim、Average|
|操作失败数|Count/Second|FailedCount|userId、instanceId|Maximum、Minimim、Average|
|内网网络入流量|Byte/s|IntranetIn|userId、instanceId|Maximum、Minimim、Average|
|写入带宽使用率|%|IntranetInRatio|userId、instanceId|Maximum、Minimim、Average|
|内网网络出流量|Byte/s|IntranetOut|userId、instanceId|Maximum、Minimum、Average|
|读取带宽使用率|%|IntranetOutRatio|userId、instanceId|Maximum、Minimum、Average|
|内存使用率|%|MemoryUsage|userId、instanceId|Maximum、Minimum、Average|
|已用连接数|Count|UsedConnection|userId、instanceId|Maximum、Minimum、Average|
|内存使用量|Byte|UsedMemory|userId、instanceId|Maximum、Minimum、Average|
|已用QPS数量|Count/Second|UsedQPS|userId、instanceId|Maximum、Minimum、Average|

