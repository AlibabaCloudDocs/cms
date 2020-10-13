# HybridDB for MySQL列表

通过本文您可以了解HybridDB for MySQL的监控项。

-   **Namespace**为**acs\_petadata**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|磁盘使用量|MB|DiskUsage|userId、instanceId|Average|
|网络流入带宽|Bytes/Second|InboundBandwidth|userId、instanceId|Average|
|子节点CPU使用率|Percent|Node\_CPUUsage|userId、instanceId、schema、nodeId|Average、Maximum|
|子节点磁盘使用量|MB|Node\_DiskUsage|userId、instanceId、schema、nodeId|Average、Maximum|
|子节点IOPS|Count/Second|Node\_IOPS|userId、instanceId、schema、nodeId|Average、Maximum|
|网络流出带宽|Bytes/Second|OutBoundBandwidth|userId、instanceId|Average|
|每秒请求数|Count/Second|QPS|userId、instanceId|Average、Maximum、Minimum|

