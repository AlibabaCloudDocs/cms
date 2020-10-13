# HBase数据同步服务

通过本文您可以了解云数据库HBase数据同步服务的监控项。

-   **Namespace**为**acs\_bds**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|每秒网络流入量|bytes/s|bytes\_in|userId、instnaceId、host|Average、Maximum、Minimum|
|每秒网络流出量|bytes/s|bytes\_out|userId、instanceId、host|Average、Maximum、Minimum|
|冷存储总容量|bytes|cold\_storage\_capacity\_bytes|userId、instanceId、host|Average、Maximum、Minimum|
|冷存储使用量|bytes|cold\_storage\_used\_bytes|userId、instanceId、host|Average、Maximum、Minimum|
|冷存储使用比例|%|cold\_storage\_used\_percent|userId、instanceId、host|Average、Maximum、Minimum|
|CPU空闲率|%|cpu\_idle|userId、instanceId、host|Average、Maximum、Minimum|
|CPU利用率System|%|cpu\_system|userId、instanceId、host|Average、Maximum、Minimum|
|CPU利用率User|%|cpu\_user|userId、instanceId、host|Average、Maximum、Minimum|
|CPU利用率IOWait|%|cpu\_wio|userId、instanceId、host|Average、Maximum、Minimum|
|失败任务数|count|failed\_job\_count|userId、instanceId、host|Average、Maximum、Minimum|
|每5分钟平均负载|1|load\_five|userId、instanceId、host|Average、Maximum、Minimum|
|每分钟平均负载|1|load\_one|userId、instanceId、host|Average、Maximum、Minimum|
|缓存大小（buff/cache）|bytes|mem\_buff\_cache|userId、instanceId、host|Average、Maximum、Minimum|
|空闲内存大小（free）|bytes|mem\_free|userId、instanceId、host|Average、Maximum、Minimum|
|共享内存大小（shared）|bytes|mem\_shared|userId、instanceId、host|Average、Maximum、Minimum|
|内存总量|bytes|mem\_total|userId、instanceId、host|Average、Maximum、Minimum|
|内存使用比例|%|mem\_used\_percent|userId、instanceId、host|Average、Maximum、Minimum|
|最大任务延迟|ms|task\_delay\_max|userId、instanceId、host|Average、Maximum、Minimum|
|异常任务数|count|warn\_job\_count|userId、instanceId、host|Average、Maximum、Minimum|
|工作节点数量|count|worker\_count|userId、instanceId、host|Average、Maximum、Minimum|

