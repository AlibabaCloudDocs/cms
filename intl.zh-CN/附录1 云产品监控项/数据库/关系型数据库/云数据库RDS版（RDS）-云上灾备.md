# 云数据库RDS版（RDS）-云上灾备

通过本文您可以了解云数据库RDS版的云上灾备的监控项。

-   **Namespace**为**acs\_rds\_dashboard**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|同步语句中的平均数据大小|Byte|AvgLogSize|userId、instanceId、direction|Average|
|同步流量|Byte/s|Flow|userId、instanceId、direction|Average|
|同步语句中的最大数据大小|Byte|MaxLogSize|userId、instanceId、direction|Average|
|同步延迟|ms|Rt|userId、instanceId、direction|Average|
|同步速度|Transactions/Second|TPS|userId、instanceId、direction|Average|

