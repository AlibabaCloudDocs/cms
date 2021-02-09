# Redis读写分离版

通过本文您可以了解云数据库Redis读写分离版的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_kvstore**。
-   **Period**默认为60秒，也可以为60的整数倍。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|数据节点平均响应时间|us|SplitrwAvgRt|userId、instanceId、nodeId|Average、Maximum|
|数据节点连接数使用率|%|SplitrwConnectionUsage|userId、instanceId、nodeId|Average、Maximum|
|数据节点CPU使用率|%|SplitrwCpuUsage|userId、instanceId、nodeId|Average、Maximum|
|数据节点命令失败次数|Count/Second|SplitrwFailedCount|userId、instanceId、nodeId|Average、Maximum|
|数据节点命中率|%|SplitrwHitRate|userId、instanceId、nodeId|Average、Maximum|
|数据节点流入带宽|KByte/s|SplitrwIntranetIn|userId、instanceId、nodeId|Average、Maximum|
|数据节点流入带宽使用率|%|SplitrwIntranetInRatio|userId、instanceId、nodeId|Average、Maximum|
|数据节点流出带宽|KByte/s|SplitrwIntranetOut|userId、instanceId、nodeId|Average、Maximum|
|数据节点流出带宽使用率|%|SplitrwIntranetOutRatio|userId、instanceId、nodeId|Average、Maximum|
|数据节点缓存内Key数量|Count|SplitrwKeys|userId、instanceId、nodeId|Average、Maximum|
|数据节点最大响应时间|us|SplitrwMaxRt|userId、instanceId、nodeId|Average、Maximum|
|数据节点内存使用率|%|SplitrwMemoryUsage|userId、instanceId、nodeId|Average、Maximum|
|Proxy单个请求的平均字节数|Byte|SplitrwProxyAvgRequestSize|userId、instanceId、nodeId|Average、Maximum|
|Proxy单个响应的平均字节数|Byte|SplitrwProxyAvgResponseSize|userId、instanceId、nodeId|Average、Maximum|
|Proxy平均时延|us|SplitrwProxyAvgRt|userId、instanceId、nodeId|Average、Maximum|
|Proxy连接数使用率|%|SplitrwProxyConnectionUsage|userId、instanceId、nodeId|Average、Maximum|
|Proxy CPU使用率|%|SplitrwProxyCpuUsage|userId、instanceId、nodeId|Average、Maximum|
|Proxy入流量速率|bit/s|SplitrwProxyIntranetIn|userId、instanceId、nodeId|Average、Maximum|
|Proxy出流量速率|bit/s|SplitrwProxyIntranetOut|userId、instanceId、nodeId|Average、Maximum|
|Proxy单个请求最大字节数|Byte|SplitrwProxyMaxRequestSize|userId、instanceId、nodeId|Average、Maximum|
|Proxy单个响应的最大字节数|Byte|SplitrwProxyMaxResponseSize|userId、instanceId、nodeId|Average、Maximum|
|Proxy最大时延|us|SplitrwProxyMaxRt|userId、instanceId、nodeId|Average、Maximum|
|Proxy每秒总请求数|Count/s|SplitrwProxyTotalQps|userId、instanceId|Average、Maximum|
|Proxy已使用连接数|Count|SplitrwProxyUsedConnection|userId、instanceId|Average、Maximum|
|数据节点QPS使用率|%|SplitrwQPSUsage|userId、instanceId、nodeId|Average、Maximum|
|数据节点已用连接数|Count|SplitrwUsedConnection|userId、instanceId、nodeId|Average、Maximum|
|数据节点内存使用量|Bytes|SplitrwUsedMemory|userId、instanceId、nodeId|Average、Maximum、Sum|
|数据节点平均每秒访问次数|Count|SplitrwUsedQPS|userId、instanceId、nodeId|Average、Maximum|

