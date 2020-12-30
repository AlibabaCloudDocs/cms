# 分析型数据库MySQL版3.0

通过本文您可以了解分析型数据库MySQL版3.0的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_adb**。
-   **Period**默认为60秒，也可以为60的整数倍。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|连接数|Count|connections|userId、instanceId|Average|
|磁盘使用率|%|disk\_used\_percent|userId、instanceId|Average|
|平均写入响应时间|Milliseconds|insert\_avg\_rt|userId、instanceId|Average|
|写入吞吐量|Mbyte|insert\_in\_bytes|userId、instanceId|Average|
|最大写入响应时间|Milliseconds|insert\_max\_rt|userId、instanceId|Average|
|QPS|Count|qps|userId、instanceId|Average|
|平均查询耗时|Milliseconds|query\_avg\_rt|userId、instanceId|Average|
|最大查询耗时|Milliseconds|query\_max\_rt|userId、instanceId|Average|
|查询等待总耗时|Milliseconds|query\_total\_wait\_time|userId、instanceId|Average|
|TPS|Count|tps|userId、instanceId|Average|
|节点CPU平均使用率|%|worker\_avg\_cpu\_used|userId、instanceId|Average|
|磁盘读吞吐量|Mbyte|worker\_avg\_read\_bytes|userId、instanceId|Average|
|磁盘平均读次数|Frequency|worker\_avg\_iops|userId、instanceId|Average|
|磁盘写吞吐量|Mbyte|worker\_avg\_bytes|userId、instanceId|Average|
|磁盘平均写次数|Frequency|worker\_avg\_iops|userId、instanceId|Average|

