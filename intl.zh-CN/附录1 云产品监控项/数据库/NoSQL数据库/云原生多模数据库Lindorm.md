# 云原生多模数据库Lindorm

通过本文您可以了解云原生多模数据库Lindorm的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_lindorm**。
-   **Period**默认为60秒，也可以为60的整数倍。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|超过Memstore上限次数|Frequency|above\_memstore\_count|userId、instanceId、host|Average、Maximum、Minimum|
|每秒网络流入量|Bytes/s|bytes\_in|userId、instanceId、host|Average、Maximum、Minimum|
|每秒网络流出量|Bytes/s|bytes\_out|userId、instanceId、host|Average、Maximum、Minimum|
|冷存储总容量|Bytes|cold\_storage\_total\_bytes|userId、instanceId、host|Average、Maximum、Minimum|
|冷存储使用量|Bytes|cold\_storage\_used\_bytes|userId、instanceId、host|Average、Maximum、Minimum|
|冷存储使用百分比|%|cold\_storage\_used\_percent|userId、instanceId、host|Average、Maximum、Minimum|
|Compaction队列长度|Count|compaction\_queue\_size|userId、instanceId、host|Average、Maximum、Minimum|
|CPU空闲率|%|cpu\_idle|userId、instanceId、host|Average、Maximum、Minimum|
|CPU利用率System|%|cpu\_system|userId、instanceId、host|Average、Maximum、Minimum|
|CPU利用率User|%|cpu\_user|userId、instanceId、host|Average、Maximum、Minimum|
|CPU利用率IOWait|%|cpu\_wio|userId、instanceId、host|Average、Maximum、Minimum|
|磁盘读流量|Bytes/s|disk\_readbytes|userId、instanceId、host|Average、Maximum、Minimum|
|磁盘写流量|Bytes/s|disk\_writebytes|userId、instanceId、host|Average、Maximum、Minimum|
|失败任务数|Count|failed\_job\_count|userId、instanceId、host|Average、Maximum、Minimum|
|Get请求量|CountS|get\_num\_ops|userId、instanceId、host|Average、Maximum、Minimum|
|Get平均RT|Milliseconds|get\_rt\_avg|userId、instanceId、host|Average、Maximum、Minimum|
|Get操作P99延迟|Milliseconds|get\_rt\_p99|userId、instanceId、host|Average、Maximum、Minimum|
|HandlerQueue长度|Count|handler\_queue\_size|userId、instanceId、host|Average、Maximum、Minimum|
|每5分钟平均负载|Load|load\_five|userId、instanceId、host|Average、Maximum、Minimum|
|每分钟平均负载|Load|load\_one|userId、instanceId、host|Average、Maximum、Minimum|
|缓存大小（Buff/Cache）|Bytes|mem\_buff\_cache|userId、instanceId、host|Average、Maximum、Minimum|
|空闲内存大小（Free）|Bytes|mem\_free|userId、instanceId、host|Average、Maximum、Minimum|
|共享内存大小（Shared）|Bytes|mem\_shared|userId、instanceId、host|Average、Maximum、Minimum|
|内存总量（Total）|Bytes|mem\_total|userId、instanceId、host|Average、Maximum、Minimum|
|内存使用比例|%|mem\_used\_percent|userId、instanceId、host|Average、Maximum、Minimum|
|Put请求量|CountS|put\_num\_ops|userId、instanceId、host|Average、Maximum、Minimum|
|Put平均RT|Milliseconds|put\_rt\_avg|userId、instanceId、host|Average、Maximum、Minimum|
|Put P99延迟|Milliseconds|put\_rt\_p99|userId、instanceId、host|Average、Maximum、Minimum|
|读流量|KB/s|read\_data\_kb|userId、instanceId、host|Average、Maximum、Minimum|
|读请求量|CountS|read\_ops|userId、instanceId、host|Average、Maximum、Minimum|
|读平均RT|Milliseconds|read\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|RegionServer管理Region个数|Count|regions\_per\_ldserver|userId、instanceId、host|Average、Maximum、Minimum|
|Scan请求量|CountS|scan\_num\_ops|userId、instanceId、host|Average、Maximum、Minimum|
|Scan平均延迟|Milliseconds|scan\_rt\_avg|userId、instanceId、host|Average、Maximum、Minimum|
|Scan P99延迟|Milliseconds|scan\_rt\_p99|userId、instanceId、host|Average、Maximum、Minimum|
|搜索每秒网络流入量|Bytes/s|search\_bytes\_in|userId、instanceId、host|Average、Maximum、Minimum|
|搜索每秒网络流出量|Bytes/s|search\_bytes\_out|userId、instanceId、host|Average、Maximum、Minimum|
|搜索CPU空闲率|%|search\_cpu\_idle|userId、instanceId、host|Average、Maximum、Minimum|
|搜索CPU利用率System|%|search\_cpu\_system|userId、instanceId、host|Average、Maximum、Minimum|
|搜索CPU利用率User|%|search\_cpu\_user|userId、instanceId、host|Average、Maximum、Minimum|
|搜索CPU利用率IOWait|%|search\_cpu\_wio|userId、instanceId、host|Average、Maximum、Minimum|
|搜索磁盘读流量|Bytes/s|search\_disk\_readbytes|userId、instanceId、host|Average、Maximum、Minimum|
|搜索磁盘写流量|Bytes/s|search\_disk\_writebytes|userId、instanceId、host|Average、Maximum、Minimum|
|搜索每5分钟平均负载|Load|search\_load\_five|userId、instanceId、host|Average、Maximum、Minimum|
|搜索每分钟平均负载|Load|search\_load\_one|userId、instanceId、host|Average、Maximum、Minimum|
|搜索缓存大小（Buff/Cache）|Bytes|search\_mem\_buff\_cache|userId、instanceId、host|Average、Maximum、Minimum|
|空闲内存大小（Free）|Bytes|search\_mem\_free|userId、instanceId、host|Average、Maximum、Minimum|
|共享内存大小（Shared）|Bytes|search\_mem\_shared|userId、instanceId、host|Average、Maximum、Minimum|
|内存总量（Total）|Bytes|search\_mem\_total|userId、instanceId、host|Average、Maximum、Minimum|
|内存使用比例|%|search\_mem\_used\_percent|userId、instanceId、host|Average、Maximum、Minimum|
|最近15分钟Select ops|CountS|search\_select\_15minRate|userId、instanceId、host|Average、Maximum、Minimum|
|最近1分钟Select ops|CountS|search\_select\_1minRate|userId、instanceId、host|Average、Maximum、Minimum|
|最近5分钟Select ops|CountS|search\_select\_5minRate|userId、instanceId、host|Average、Maximum、Minimum|
|Select次数总计|Count|search\_select\_count|userId、instanceId、host|Average、Maximum、Minimum|
|Select最大RT|Milliseconds|search\_select\_max\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Select平均ops|CountS|search\_select\_meanRate|userId、instanceId、host|Average、Maximum、Minimum|
|Select平均RT|Milliseconds|search\_select\_mean\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Select p75 RT|Milliseconds|search\_select\_p75\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Select p95 RT|Milliseconds|search\_select\_p95\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Select p999 RT|Milliseconds|search\_select\_p999\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Select p99 RT|Milliseconds|search\_select\_p99\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|最近15分钟Update ops|CountS|search\_update\_15minRate|userId、instanceId、host|Average、Maximum、Minimum|
|最近1分钟Update ops|CountS|search\_update\_1minRate|userId、instanceId、host|Average、Maximum、Minimum|
|最近5分钟Update ops|CountS|search\_update\_5minRate|userId、instanceId、host|Average、Maximum、Minimum|
|Update次数总计|Count|search\_update\_count|userId、instanceId、host|Average、Maximum、Minimum|
|Update最大RT|Milliseconds|search\_update\_max\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Update平均ops|CountS|search\_update\_meanRate|userId、instanceId、host|Average、Maximum、Minimum|
|Update平均RT|Milliseconds|search\_update\_mean\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Update P75 RT|Milliseconds|search\_update\_p75\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Update P95 RT|Milliseconds|search\_update\_p95\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Update P999 RT|Milliseconds|search\_update\_p999\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Update P99 RT|Milliseconds|search\_update\_p99\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Solr每秒网络流入量|Bytes/s|solr\_bytes\_in|userId、instanceId、host|Average、Maximum、Minimum|
|Solr每秒网络流出量|Bytes/s|solr\_bytes\_out|userId、instanceId、host|Average、Maximum、Minimum|
|Solr CPU空闲率|%|solr\_cpu\_idle|userId、instanceId、host|Average、Maximum、Minimum|
|Solr CPU利用率System|%|solr\_cpu\_system|userId、instanceId、host|Average、Maximum、Minimum|
|Solr CPU利用率User|%|solr\_cpu\_user|userId、instanceId、host|Average、Maximum、Minimum|
|Solr CPU利用率IOWait|%|solr\_cpu\_wio|userId、instanceId、host|Average、Maximum、Minimum|
|Solr磁盘读流量|Bytes/s|solr\_disk\_readbytes|userId、instanceId、host|Average、Maximum、Minimum|
|Solr磁盘写流量|Bytes/s|solr\_disk\_writebytes|userId、instanceId、host|Average、Maximum、Minimum|
|Solr每5分钟平均负载|Load|solr\_load\_five|userId、instanceId、host|Average、Maximum、Minimum|
|Solr每分钟平均负载|Load|solr\_load\_one|userId、instanceId、host|Average、Maximum、Minimum|
|缓存大小（Buff/Cache）|Bytes|solr\_mem\_buff\_cache|userId、instanceId、host|Average、Maximum、Minimum|
|空闲内存大小（Free）|Bytes|solr\_mem\_free|userId、instanceId、host|Average、Maximum、Minimum|
|共享内存大小（Shared）|Bytes|solr\_mem\_shared|userId、instanceId、host|Average、Maximum、Minimum|
|内存总量（Total）|Bytes|solr\_mem\_total|userId、instanceId、host|Average、Maximum、Minimum|
|内存使用比例|%|solr\_mem\_used\_percent|userId、instanceId、host|Average、Maximum、Minimum|
|最近15分钟Select ops|CountS|solr\_select\_15minRate|userId、instanceId、host|Average、Maximum、Minimum|
|最近1分钟Select ops|CountS|solr\_select\_1minRate|userId、instanceId、host|Average、Maximum、Minimum|
|最近5分钟Select ops|CountS|solr\_select\_5minRate|userId、instanceId、host|Average、Maximum、Minimum|
|Select次数总计|Count|solr\_select\_count|userId、instanceId、host|Average、Maximum、Minimum|
|Select最大RT|Milliseconds|solr\_select\_max\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Select平均ops|CountS|solr\_select\_meanRate|userId、instanceId、host|Average、Maximum、Minimum|
|Select平均RT|Milliseconds|solr\_select\_mean\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Select P75 RT|Milliseconds|solr\_select\_p75\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Select P95 RT|Milliseconds|solr\_select\_p95\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Select P999 RT|Milliseconds|solr\_select\_p999\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Select P99 RT|Milliseconds|solr\_select\_p99\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Solr存储空间总量|Bytes|solr\_storage\_total\_bytes|userId、instanceId、host|Average、Maximum、Minimum|
|Solr存储空间使用量|Bytes|solr\_storage\_used\_bytes|userId、instanceId、host|Average、Maximum、Minimum|
|Solr存储空间使用比例|%|solr\_storage\_used\_percent|userId、instanceId、host|Average、Maximum、Minimum|
|最近15分钟Update ops|CountS|solr\_update\_15minRate|userId、instanceId、host|Average、Maximum、Minimum|
|最近1分钟Update ops|CountS|solr\_update\_1minRate|userId、instanceId、host|Average、Maximum、Minimum|
|最近5分钟Update ops|CountS|solr\_update\_5minRate|userId、instanceId、host|Average、Maximum、Minimum|
|Update次数总计|Count|solr\_update\_count|userId、instanceId、host|Average、Maximum、Minimum|
|Update最大RT|Milliseconds|solr\_update\_max\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Update平均ops|CountS|solr\_update\_meanRate|userId、instanceId、host|Average、Maximum、Minimum|
|Update平均RT|Milliseconds|solr\_update\_mean\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Update p75 RT|Milliseconds|solr\_update\_p75\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Update p95 RT|Milliseconds|solr\_update\_p95\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Update p999 RT|Milliseconds|solr\_update\_p999\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Update p99 RT|Milliseconds|solr\_update\_p99\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|存储空间总量|Bytes|storage\_total\_bytes|userId、instanceId、host|Average、Maximum、Minimum|
|存储空间使用量|Bytes|storage\_used\_bytes|userId、instanceId、host|Average、Maximum、Minimum|
|存储空间使用比例|%|storage\_used\_percent|userId、instanceId、host|Average、Maximum、Minimum|
|存储本地化率|%|store\_locality|userId、instanceId、host|Average、Maximum、Minimum|
|最大任务延迟|ms|task\_delay\_max|userId、instanceId、host|Average、Maximum、Minimum|
|数据点数量|Count|tsdb\_datapoints\_added|userId、instanceId、host|Average、Maximum、Minimum|
|磁盘使用量|Gbyte|tsdb\_disk\_used|userId、instanceId、host|Average、Maximum、Minimum|
|JVM内存使用率|%|tsdb\_jvm\_used\_percent|userId、instanceId、host|Average、Maximum、Minimum|
|异常任务数|Count|warn\_job\_count|userId、instanceId、host|Average、Maximum、Minimum|
|工作节点数量|Count|worker\_count|userId、instanceId、host|Average、Maximum、Minimum|
|写流量|KB/s|write\_data\_kb|userId、instanceId、host|Average、Maximum、Minimum|
|写请求量|CountS|write\_ops|userId、instanceId、host|Average、Maximum、Minimum|
|写平均RT|Milliseconds|write\_rt|userId、instanceId、host|Average、Maximum、Minimum|

