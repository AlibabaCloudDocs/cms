# Redis标准版

通过本文您可以了解云数据库Redis标准版的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_kvstore**。
-   **Period**默认为60秒，也可以为60的整数倍。

**说明：** 云监控只支持2.8以上版本的Redis实例。2.8版本的Redis实例已停止售卖。更多信息，请参见[【通知】2.8版本Redis实例停止售卖](/intl.zh-CN/产品通知/【通知】2.8版本Redis实例停止售卖.md)。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|平均响应时间|us|StandardAvgRt|userId、instanceId|Average、Maximum|
|连接数使用率|%|StandardConnectionUsage|userId、instanceId|Average、Maximum|
|CPU使用率|%|StandardCpuUsage|userId、instanceId|Average、Maximum|
|命令失败次数|Count/Second|StandardFailedCount|userId、instanceId|Average、Maximum|
|命中率|%|StandardHitRate|userId、instanceId|Average、Maximum|
|入方向流量|KByte/s|StandardIntranetIn|userId、instanceId|Average、Maximum|
|流入带宽使用率|%|StandardIntranetInRatio|userId、instanceId|Average、Maximum|
|出方向流量|KByte/s|StandardIntranetOut|userId、instanceId|Average、Maximum|
|流出带宽使用率|%|StandardIntranetOutRatio|userId、instanceId|Average、Maximum|
|缓存内Key数量|个|StandardKeys|userId、instanceId|Average、Maximum|
|最大响应时间|us|StandardMaxRt|userId、instanceId|Average、Maximum|
|内存使用率|%|StandardMemoryUsage|userId、instanceId|Average、Maximum|
|QPS使用率|%|StandardQPSUsage|userId、instanceId|Average、Maximum|
|已用连接数|个|StandardUsedConnection|userId、instanceId|Average、Maximum|
|内存使用量|Bytes|StandardUsedMemory|userId、instanceId|Average、Maximum|
|平均每秒访问次数|个|StandardUsedQPS|userId、instanceId|Average、Maximum|

