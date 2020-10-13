# Earlier ApsaraDB for Memcache

This topic describes the metrics for ApsaraDB for Memcache of the earlier version.

-   Set the **Namespace** parameter to **acs\_memcache**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|Eviction|CountSecond|Evict|userId and instanceId|Maximum, Minimum, and Average|
|Read Hit Rate|%|HitRate|userId and instanceId|Maximum, Minimum, and Average|
|Cache Inbound Bandwidth|Byte/s|IntranetIn|userId and instanceId|Maximum, Minimum, and Average|
|Cache Outbound Bandwidth|Byte/s|IntranetOut|userId and instanceId|Maximum, Minimum, and Average|
|Number of Records|Count|ItemCount|userId and instanceId|Maximum, Minimum, and Average|
|Cache Used|Byte|UsedMemCache|userId and instanceId|Maximum, Minimum, and Average|
|QPS|Count/s|UsedQps|userId and instanceId|Maximum, Minimum, and Average|

