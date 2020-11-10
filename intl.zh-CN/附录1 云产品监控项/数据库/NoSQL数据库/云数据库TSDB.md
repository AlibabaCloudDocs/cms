# 云数据库TSDB

通过本文您可以了解时序时空数据库TSDB的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_hitsdb**。
-   **Period**默认为60秒，也可以为60的整数倍。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|时间点增量|Count|DataPointsIncrement|userId、instanceId、database|Value|
|磁盘使用量|GB|DiskUtilization|userId、instanceId|Value|
|时间线数量|Count|TotalTimeSeries|userId、instanceId、database|Value|
|CPU使用率|%|CpuUsage|userId、instanceId、host|Maximum|
|内存使用率|%|MemUsage|userId、instanceId、host|Maximum|
|TSDB-内存使用率|%|MemUsage-TSDB|instanceId、host|Maximum|

