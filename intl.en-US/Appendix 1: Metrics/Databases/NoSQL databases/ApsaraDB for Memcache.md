# ApsaraDB for Memcache

This topic describes the metrics for ApsaraDB for Memcache.

-   Set the **Namespace** parameter to **acs\_memcache**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Connection Usage|%|ConnectionUsage|userId and instanceId|Maximum, Minimum, and Average|
|CPU Usage|%|CpuUsage|userId and instanceId|Maximum, Minimum, and Average|
|Failed operations|count|FailedCount|userId and instanceId|Maximum, Minimum, and Average|
|HitRate|%|HitRate|userId and instanceId|Maximum, Minimum, and Average|
|Inbound Bandwidth|byte/s|IntranetIn|userId and instanceId|Maximum, Minimum, and Average|
|Inbound Bandwidth Usage|%|IntranetInRatio|userId and instanceId|Maximum, Minimum, and Average|
|Outbound Bandwidth|byte/s|IntranetOut|userId and instanceId|Maximum, Minimum, and Average|
|Outbound Bandwidth Usage|%|IntranetOutRatio|userId and instanceId|Maximum, Minimum, and Average|
|Memory Usage|%|MemoryUsage|userId and instanceId|Maximum, Minimum, and Average|
|Connected|count|UsedConnection|userId and instanceId|Maximum, Minimum, and Average|
|Memory Usage|byte|UsedMemory|userId and instanceId|Maximum, Minimum, and Average|

