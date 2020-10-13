# 旧版云数据库Memcache

通过本文您可以了解旧版云数据库Memcache的监控项。

-   **Namespace**为**acs\_memcache**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|逐出|CountSecond|Evict|userId、instanceId|Maximum、Minimum、Average|
|读取命中率|%|HitRate|userId、instanceId|Maximum、Minimum、Average|
|内网网络入流量|Byte/s|IntranetIn|userId、instanceId|Maximum、Minimum、Average|
|内网网络出流量|Byte/s|IntranetOut|userId、instanceId|Maximum、Minimum、Average|
|记录数|Count|ItemCount|userId、instanceId|Maximum、Minimum、Average|
|已用缓存|Byte|UsedMemCache|userId、instanceId|Maximum、Minimum、Average|
|QPS|Count/s|UsedQps|userId、instanceId|Maximum、Minimum、Average|

