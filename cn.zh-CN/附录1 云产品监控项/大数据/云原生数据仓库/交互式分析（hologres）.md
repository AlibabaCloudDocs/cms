# 交互式分析（hologres）

通过本文您可以了解交互式分析Hologres的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_hologres**。
-   **Period**默认为60秒，也可以为60的整数倍。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|连接数|Count|connection\_count|userId、instanceId、dbName|Average、Sum|
|SQL总连接数|Count|connection\_num|userId、instanceId|Average|
|CPU水位|%|cpu\_usage|userId、instanceId|Average|
|Delete语句QPS|CountSecond|delete\_qps|userId、instanceId|Average|
|Delete语句响应时间|MilliSeconds|delete\_query\_latency|userId、instanceId|Average、Maximum|
|每秒Delete记录数|CountS|delete\_record\_qps|userId、instanceId|Average|
|失败查询数|Count|failed\_queries|userId、instanceId|Average|
|Insert语句QPS|CountSecond|insert\_qps|userId、instanceId|Average|
|Insert语句响应时间|MilliSeconds|insert\_query\_latency|userId、instanceId|Average、Maximum|
|内存水位|%|memory\_usage|userId、instanceId|Average|
|Query响应时间明细|MilliSeconds|query\_latency|instanceId、userId、cmdType|Average|
|Query QPS明细|CountS|query\_qps|instanceId、userId、cmdType|Average|
|每秒实时导入吞吐量|Bytes|realtime\_ingestion\_throughput|userId、instanceId|Average|
|实时导入RPS|CountS|record\_input\_qps|instanceId、userId|Average|
|每秒Insert记录数|CountS|records\_per\_second|userId、instanceId|Average|
|查询时长P99|Seconds|select\_latency|userId、instanceId|Maximum|
|查询时长P95|Seconds|select\_latency\_p95|userId、instanceId|Maximum|
|查询时长P999|Seconds|select\_latency\_p999|userId、instanceId|Maximum|
|Select语句QPS|CountSecond|select\_qps|userId、instanceId|Average|
|Select语句响应时间|MilliSeconds|select\_query\_latency|instanceId、userId|Average|
|存储已用容量|Bytes|storage\_usage|userId、instanceId|Average|
|存储水位|%|storage\_usage\_percent|userId、instanceId|Average|
|Update语句QPS|CountSecond|update\_qps|userId、instanceId|Average|
|Update语句响应时间|MilliSeconds|update\_query\_latency|userId、instanceId|Average、Maximum|
|每秒Update记录数|CountS|update\_record\_qps|userId、instanceId|Average|

