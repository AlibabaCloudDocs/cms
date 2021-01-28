# 阿里云LogstashService

通过本文您可以了解阿里云LogstashService的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_elasticsearch**。
-   **Period**默认为60秒，也可以为60的整数倍。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|节点CPU使用率|%|LogstashCpuPercent|userId、instanceId、nodeHost|Maximum|
|节点磁盘使用率|%|LogstashNodeDiskUsage|userId、instanceId、nodeHost|Maximum|
|节点内存使用量|%|LogstashNodeHeapMemory|userId、instanceId、nodeHost|Maximum|
|节点1分钟负载|Value|LogstashNodeLoad1m|userId、instanceId、nodeHost|Maximum|

