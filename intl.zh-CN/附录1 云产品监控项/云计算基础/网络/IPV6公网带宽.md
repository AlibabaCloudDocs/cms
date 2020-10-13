# IPV6公网带宽

通过本文您可以了解IPV6公网带宽的监控项。

-   **Namespace**为**acs\_ipv6\_bandwidth**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|公网流入数据包数|pps|Ipv6Gateway.PkgsInFromInternet|userId、instanceId|Value|
|公网流出数据包数|pps|Ipv6Gateway.PkgsOutToInternet|userId、instanceId|Value|
|公网丢弃流入数据包|pps|Ipv6Gateway.RateDropInFromInternet|userId、instanceId|Value|
|公网丢弃流出数据包|pps|Ipv6Gateway.RateDropOutFromInternet|userId、instanceId|Value|
|公网流入流量|bits/s|Ipv6Gateway.RateInFromInternet|userId、instanceId|Value|
|公网限速丢弃流入数据包|pps|Ipv6Gateway.RateLimitedPkgsDropInFromInternet|userId、instanceId|Value|
|公网限速丢弃流出数据包|pps|Ipv6Gateway.RateLimitedPkgsDropOutToInternet|userId、instanceId|Value|
|公网流出流量|bits/s|Ipv6Gateway.RateOutToInternet|userId、instanceId|Value|
|公网流入带宽利用率|Value|Ipv6Gateway.RatePercentageInFromInternet|userId、instanceId|Value|
|公网流出带宽利用率|Value|Ipv6Gateway.RatePercentageOutToInternet|userId、instanceId|Value|

