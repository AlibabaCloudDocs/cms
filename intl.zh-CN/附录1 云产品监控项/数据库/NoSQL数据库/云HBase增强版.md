# 云HBase增强版

通过本文您可以了解云数据库HBase增强版的监控项。

-   **Namespace**为**acs\_hbaseue**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|超过memstore上限次数|frequency|above\_memstore\_count|userId、instanceId、host|Average、Maximum、Minimum|
|每秒网络流入量|bytes/s|bytes\_in|userId、instanceId、host|Average、Maximum、Minimum|
|每秒网络流出量|bytes/s|bytes\_out|userId、instanceId、host|Average、Maximum、Minimum|
|冷存储总容量|bytes|cold\_storage\_total\_bytes|userId、instanceId、host|Average、Maximum、Minimum|
|冷存储使用量|bytes|cold\_storage\_used\_bytes|userId、instanceId、host|Average、Maximum、Minimum|
|冷存储使用百分比|%|cold\_storage\_used\_percent|userId、instanceId、host|Average、Maximum、Minimum|
|Compaction队列长度|count|compaction\_queue\_size|userId、instanceId、host|Average、Maximum、Minimum|
|CPU空闲率|%|cpu\_idle|userId、instanceId、host|Average、Maximum、Minimum|
|CPU利用率System|%|cpu\_system|userId、instanceId、host|Average、Maximum、Minimum|
|CPU利用率User|%|cpu\_user|userId、instanceId、host|Average、Maximum、Minimum|
|CPU利用率IOWait|%|cpu\_wio|userId、instanceId、host|Average、Maximum、Minimum|
|磁盘读流量|bytes/s|disk\_readbytes|userId、instanceId、host|Average、Maximum、Minimum|
|磁盘写流量|bytes/s|disk\_writebytes|userId、instanceId、host|Average、Maximum、Minimum|
|Get请求量|countS|get\_num\_ops|userId、instanceId、host|Average、Maximum、Minimum|
|Get平均RT|milliseconds|get\_rt\_avg|userId、instanceId、host|Average、Maximum、Minimum|
|Get操作P99延迟|milliseconds|get\_rt\_p99|userId、instanceId、host|Average、Maximum、Minimum|
|HandlerQueue长度|count|handler\_queue\_size|userId、instanceId、host|Average、Maximum、Minimum|
|每5分钟平均负载|load|load\_five|userId、instanceId、host|Average、Maximum、Minimum|
|每分钟平均负载|load|load\_one|userId、instanceId、host|Average、Maximum、Minimum|
|缓存大小（buff/cache）|bytes|mem\_buff\_cache|userId、instanceId、host|Average、Maximum、Minimum|
|空闲内存大小（free）|bytes|mem\_free|userId、instanceId、host|Average、Maximum、Minimum|
|共享内存大小（shared）|bytes|mem\_shared|userId、instanceId、host|Average、Maximum、Minimum|
|内存总量（total）|bytes|mem\_total|userId、instanceId、host|Average、Maximum、Minimum|
|内存使用比例|%|mem\_used\_percent|userId、instanceId、host|Average、Maximum、Minimum|
|Put请求量|countS|put\_num\_ops|userId、instanceId、host|Average、Maximum、Minimum|
|Put平均RT|milliseconds|put\_rt\_avg|userId、instanceId、host|Average、Maximum、Minimum|
|Put P99延迟|milliseconds|put\_rt\_p99|userId、instanceId、host|Average、Maximum、Minimum|
|读流量|KB/s|read\_data\_kb|userId、instanceId、host|Average、Maximum、Minimum|
|读请求量|countS|read\_ops|userId、instanceId、host|Average、Maximum、Minimum|
|读平均RT|milliseconds|read\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|RegionServer管理Region个数|count|regions\_per\_ldserver|userId、instanceId、host|Average、Maximum、Minimum|
|Scan请求量|countS|scan\_num\_ops|userId、instanceId、host|Average、Maximum、Minimum|
|Scan平均延迟|milliseconds|scan\_rt\_avg|userId、instanceId、host|Average、Maximum、Minimum|
|Scan P99延迟|milliseconds|scan\_rt\_p99|userId、instanceId、host|Average、Maximum、Minimum|
|Solr每秒网络流入量|bytes/s|solr\_bytes\_in|userId、instanceId、host|Average、Maximum、Minimum|
|Solr每秒网络流出量|bytes/s|solr\_bytes\_out|userId、instanceId、host|Average、Maximum、Minimum|
|Solr CPU空闲率|%|solr\_cpu\_idle|userId、instanceId、host|Average、Maximum、Minimum|
|Solr CPU利用率System|%|solr\_cpu\_system|userId、instanceId、host|Average、Maximum、Minimum|
|Solr CPU利用率User|%|solr\_cpu\_user|userId、instanceId、host|Average、Maximum、Minimum|
|Solr CPU利用率IOWait|%|solr\_cpu\_wio|userId、instanceId、host|Average、Maximum、Minimum|
|Solr磁盘读流量|bytes/s|solr\_disk\_readbytes|userId、instanceId、host|Average、Maximum、Minimum|
|Solr磁盘写流量|bytes/s|solr\_disk\_writebytes|userId、instanceId、host|Average、Maximum、Minimum|
|Solr每5分钟平均负载|load|solr\_load\_five|userId、instanceId、host|Average、Maximum、Minimum|
|Solr每分钟平均负载|load|solr\_load\_one|userId、instanceId、host|Average、Maximum、Minimum|
|缓存大小（buff/cache）|bytes|solr\_mem\_buff\_cache|userId、instanceId、host|Average、Maximum、Minimum|
|空闲内存大小（free）|bytes|solr\_mem\_free|userId、instanceId、host|Average、Maximum、Minimum|
|共享内存大小（shared）|bytes|solr\_mem\_shared|userId、instanceId、host|Average、Maximum、Minimum|
|内存总量（total）|bytes|solr\_mem\_total|userId、instanceId、host|Average、Maximum、Minimum|
|内存使用比例|%|solr\_mem\_used\_percent|userId、instanceId、host|Average、Maximum、Minimum|
|最近15分钟select ops|countS|solr\_select\_15minRate|userId、instanceId、host|Average、Maximum、Minimum|
|最近1分钟select ops|countS|solr\_select\_1minRate|userId、instanceId、host|Average、Maximum、Minimum|
|最近5分钟select ops|countS|solr\_select\_5minRate|userId、instanceId、host|Average、Maximum、Minimum|
|Select次数总计|count|solr\_select\_count|userId、instanceId、host|Average、Maximum、Minimum|
|Select最大RT|milliseconds|solr\_select\_max\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Select平均ops|countS|solr\_select\_meanRate|userId、instanceId、host|Average、Maximum、Minimum|
|Select平均RT|milliseconds|solr\_select\_mean\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Select p75 RT|milliseconds|solr\_select\_p75\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Select p95 RT|milliseconds|solr\_select\_p95\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Select p999 RT|milliseconds|solr\_select\_p999\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Select p99 RT|milliseconds|solr\_select\_p99\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Solr存储空间总量|bytes|solr\_storage\_total\_bytes|userId、instanceId、host|Average、Maximum、Minimum|
|Solr存储空间使用量|bytes|solr\_storage\_used\_bytes|userId、instanceId、host|Average、Maximum、Minimum|
|Solr存储空间使用比例|%|solr\_storage\_used\_percent|userId、instanceId、host|Average、Maximum、Minimum|
|最近15分钟update ops|countS|solr\_update\_15minRate|userId、instanceId、host|Average、Maximum、Minimum|
|最近1分钟update ops|countS|solr\_update\_1minRate|userId、instanceId、host|Average、Maximum、Minimum|
|最近5分钟update ops|countS|solr\_update\_5minRate|userId、instanceId、host|Average、Maximum、Minimum|
|Update次数总计|count|solr\_update\_count|userId、instanceId、host|Average、Maximum、Minimum|
|Update最大RT|milliseconds|solr\_update\_max\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Update平均ops|countS|solr\_update\_meanRate|userId、instanceId、host|Average、Maximum、Minimum|
|Update平均RT|milliseconds|solr\_update\_mean\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Update p75 RT|milliseconds|solr\_update\_p75\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Update p95 RT|milliseconds|solr\_update\_p95\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Update p999 RT|milliseconds|solr\_update\_p999\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|Update p99 RT|milliseconds|solr\_update\_p99\_rt|userId、instanceId、host|Average、Maximum、Minimum|
|存储空间总量|bytes|storage\_total\_bytes|userId、instanceId、host|Average、Maximum、Minimum|
|存储空间使用量|bytes|storage\_used\_bytes|userId、instanceId、host|Average、Maximum、Minimum|
|存储空间使用比例|%|storage\_used\_percent|userId、instanceId、host|Average、Maximum、Minimum|
|存储本地化率|%|store\_locality|userId、instanceId、host|Average、Maximum、Minimum|
|写流量|KB/s|write\_data\_kb|userId、instanceId、host|Average、Maximum、Minimum|
|写请求量|countS|write\_ops|userId、instanceId、host|Average、Maximum、Minimum|

