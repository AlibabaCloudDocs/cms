# Redis读写分离版

通过本文您可以了解云数据库Redis读写分离版的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_kvstore**。
-   **Period**默认为60秒，也可以为60的整数倍。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|平均响应时间|us|SplitrwAvgRt|userId、instanceId、nodeId|Average、Maximum|
|连接数使用率|%|SplitrwConnectionUsage|userId、instanceId、nodeId|Average、Maximum|
|CPU使用率|%|SplitrwCpuUsage|userId、instanceId、nodeId|Average、Maximum|
|命令失败次数|Count/Second|SplitrwFailedCount|userId、instanceId、nodeId|Average、Maximum|
|命中率|%|SplitrwHitRate|userId、instanceId、nodeId|Average、Maximum|
|入方向流量|KByte/s|SplitrwIntranetIn|userId、instanceId、nodeId|Average、Maximum|
|流入带宽使用率|%|SplitrwIntranetInRatio|userId、instanceId、nodeId|Average、Maximum|
|出方向流量|KByte/s|SplitrwIntranetOut|userId、instanceId、nodeId|Average、Maximum|
|流出带宽使用率|%|SplitrwIntranetOutRatio|userId、instanceId、nodeId|Average、Maximum|
|缓存内Key数量|Count|SplitrwKeys|userId、instanceId、nodeId|Average、Maximum|
|最大响应时间|us|SplitrwMaxRt|userId、instanceId、nodeId|Average、Maximum|
|内存使用率|%|SplitrwMemoryUsage|userId、instanceId、nodeId|Average、Maximum|
|QPS使用率|%|SplitrwQPSUsage|userId、instanceId、nodeId|Average、Maximum|
|已用连接数|Count|SplitrwUsedConnection|userId、instanceId、nodeId|Average、Maximum|
|内存使用量|Bytes|SplitrwUsedMemory|userId、instanceId、nodeId|Average、Maximum、Sum|
|平均每秒访问次数|Count|SplitrwUsedQPS|userId、instanceId、nodeId|Average、Maximum|

