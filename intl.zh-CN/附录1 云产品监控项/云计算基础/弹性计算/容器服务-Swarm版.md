# 容器服务-Swarm版

通过本文您可以了解容器服务Swarm版的监控项。

-   **Namespace**为**acs\_containerservice\_dashboard**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|GPU内存使用量|Bytes|ContainerGPUMemoryUsed|userId、clusterId、serviceId、instanceId、gpuId|Average|
|CPU使用率|%|CpuUtilization|userId、clusterId、serviceId、instanceId|Average、Minimum、Maximum|
|IO读取|bits/s|IORead|userId、clusterId、serviceId、instanceId|Average、Minimum、Maximum|
|容器IO读速率|Bytes/s|IOReadRate|userId、clusterId、serviceId、instanceId|Average、Minimum、Maximum|
|IO写入|bits/s|IOWrite|userId、clusterId、serviceId、instanceId|Average、Minimum、Maximum|
|容器IO写速率|Bytes|IOWriteRate|userId、clusterId、serviceId、instanceId|Average、Minimum、Maximum|
|网络流入流量|Bytes|InternetIn|userId、clusterId、serviceId、instanceId|Average、Sum、Minimum、Maximum|
|网络流入速率|bits/s|InternetInRate|userId、clusterId、serviceId、instanceId|Average、Minimum、Maximum|
|网络流出流量|Bytes/s|InternetOut|userId、clusterId、serviceId、instanceId|Average、Minimum、Maximum|
|网络流出速率|bits/s|InternetOutRate|userId、clusterId、serviceId、instanceId|Average、Minimum、Maximum|
|内存|Bytes|MemoryAmount|userId、clusterId、serviceId、instanceId|Average、Minimum、Maximum|
|内存使用百分比|%|MemoryUtilization|userId、clusterId、serviceId、InstanceId|Average、Minimum、Maximum|

