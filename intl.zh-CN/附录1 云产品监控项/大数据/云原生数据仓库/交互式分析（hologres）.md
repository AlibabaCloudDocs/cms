# 交互式分析（hologres）

通过本文您可以了解交互式分析Hologres的监控项。

-   **Namespace**为**acs\_hologres**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|SQL连接数|个|connection\_num|userId、instanceId|Average|
|CPU水位|%|cpu\_usage|userId、instanceId|Average|
|Delete SQL QPS|CountSecond|delete\_qps|userId、instanceId|Average|
|失败查询/秒|CountSecond|failed\_queries|userId、instanceId|Average|
|Insert SQL QPS|CountSecond|insert\_qps|userId、instanceId|Average|
|内存水位|%|memory\_usage|userId、instanceId|Average|
|插入RPS|CountSecond|records\_per\_second|userId、instanceId|Average|
|查询时长P99|Seconds|select\_latency|userId、instanceId|Maximum|
|查询时长P95|Seconds|select\_latency\_p95|userId、instanceId|Maximum|
|查询时长P999|Seconds|select\_latency\_p999|userId、instanceId|Maximum|
|Select SQL QPS|CountSecond|select\_qps|userId、instanceId|Average|
|存储水位|%|storage\_usage\_percent|userId、instanceId|Average|
|Update SQL QPS|CountSecond|update\_qps|userId、instanceId|Average|
|存储已用容量|MB|storage\_usage|userId、instanceId|Average|

