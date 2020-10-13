# MaxCompute-包年包月Quota组资源

通过本文您可以了解大数据计算服务MaxCompute的包年包月Quota组资源的监控项。

-   **Namespace**为**acs\_maxcompute\_prepay**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|预付费配额组CPU使用量|%|PrePayQuotaGroupCPUUsed|userId、groupName|Average|
|包年包月配额组作业等待数|Count|PrePayQuotaGroupJobWaitQueue|userId、groupName|Value|
|包年包月配额组内存使用量|MB|PrePayQuotaGroupMemUsed|userId、groupName|Average|

