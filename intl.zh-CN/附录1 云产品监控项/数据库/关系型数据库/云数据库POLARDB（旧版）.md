# 云数据库POLARDB（旧版）

通过本文您可以了解旧版云数据库POLARDB的监控项。

-   **Namespace**为**acs\_polardb**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|连接数使用率|%|instance\_connection\_utilization|userId、instanceId|Maximum、Minimum、Average|
|CPU使用率|%|instance\_cpu\_utilization|userId、instanceId|Average|
|网络流入带宽|bit/s|instance\_input\_bandwidth|userId、instanceId|Average|
|内存使用率|%|instance\_memory\_utilization|userId、instanceId|Average|
|网络流出带宽|bit/s|instance\_output\_bandwidth|userId、instanceId|Average|

