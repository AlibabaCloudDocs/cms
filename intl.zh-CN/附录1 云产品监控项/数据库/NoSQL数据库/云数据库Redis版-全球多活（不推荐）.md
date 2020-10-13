# 云数据库Redis版-全球多活（不推荐）

通过本文您可以了解云数据库Redis版的全球多活实例的监控项。

-   **Namespace**为**acs\_kvstore**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|同步语句中的平均数据大小|Byte|AvgLogSize|userId、instanceId、direction|Average|
|同步流量|Byte/s|Flow|userId、instanceId、direction|Average|
|同步语句中的最大数据大小|Byte|MaxLogSize|userId、instanceId、direction|Average|
|同步延迟|ms|Rt|userId、instanceId、direction|Average|
|同步速度|Transactions/Second|TPS|userId、instanceId、direction|Average|

