# Container Service

This topic describes the metrics for Container Service for Swarm.

-   Set the **Namespace** parameter to **acs\_containerservice\_dashboard**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|GPU Memory Usage|Bytes|ContainerGPUMemoryUsed|userId, clusterId, serviceId, instanceId, and gpuId|Average|
|CPU Usage|%|CpuUtilization|userId, clusterId, serviceId, and instanceId|Average, Minimum, and Maximum|
|I/O Read|bits/s|IORead|userId, clusterId, serviceId, and instanceId|Average, Minimum, and Maximum|
|I/O Read Rate|Bytes/s|IOReadRate|userId, clusterId, serviceId, and instanceId|Average, Minimum, and Maximum|
|I/O Write|bits/s|IOWrite|userId, clusterId, serviceId, and instanceId|Average, Minimum, and Maximum|
|I/O Write Rate|Bytes|IOWriteRate|userId, clusterId, serviceId, and instanceId|Average, Minimum, and Maximum|
|Inbound Traffic|Bytes|InternetIn|userId, clusterId, serviceId, and instanceId|Average, Sum, Minimum, and Maximum|
|Internet Inbound Rate|bits/s|InternetInRate|userId, clusterId, serviceId, and instanceId|Average, Minimum, and Maximum|
|Outbound Traffic|Bytes/s|InternetOut|userId, clusterId, serviceId, and instanceId|Average, Minimum, and Maximum|
|Internet Outbound Rate|bits/s|InternetOutRate|userId, clusterId, serviceId, and instanceId|Average, Minimum, and Maximum|
|Memory|Bytes|MemoryAmount|userId, clusterId, serviceId, and instanceId|Average, Minimum, and Maximum|
|Memory Usage|%|MemoryUtilization|userId, clusterId, serviceId, and instanceId|Average, Minimum, and Maximum|

