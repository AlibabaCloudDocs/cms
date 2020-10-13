# MaxCompute-按量付费

通过本文您可以了解大数据计算服务MaxCompute的按量付费的监控项。

-   **Namespace**为**acs\_maxcompute\_prepay**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|按量付费日作业消费|rmb|TaskDailyCost|userId、project|Maximum|
|按量付费月作业消费|rmb|TaskMonthlyCost|userId、project|Maximum|

