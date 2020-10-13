# ipv6\_bandwidth

This topic describes the metrics for IPv6 Internet bandwidth.

-   Set the **Namespace** parameter to **acs\_ipv6\_bandwidth**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|PkgsInFromInternet|packet/s|Ipv6Gateway.PkgsInFromInternet|userId and instanceId|Value|
|PkgsOutToInternet|packet/s|Ipv6Gateway.PkgsOutToInternet|userId and instanceId|Value|
|RateDropInFromInternet|packet/s|Ipv6Gateway.RateDropInFromInternet|userId and instanceId|Value|
|RateDropInFromInternet|packet/s|Ipv6Gateway.RateDropOutFromInternet|userId and instanceId|Value|
|RateInFromInternet|bits/s|Ipv6Gateway.RateInFromInternet|userId and instanceId|Value|
|RateLimitedPkgsDropInFromInternet|packet/s|Ipv6Gateway.RateLimitedPkgsDropInFromInternet|userId and instanceId|Value|
|RateLimitedPkgsDropOutToInternet|packet/s|Ipv6Gateway.RateLimitedPkgsDropOutToInternet|userId and instanceId|Value|
|RateOutToInternet|bits/s|Ipv6Gateway.RateOutToInternet|userId and instanceId|Value|
|Public Network Inbound Traffic Percentage|value|Ipv6Gateway.RatePercentageInFromInternet|userId and instanceId|Value|
|Public Network Outbound Traffic Percentage|value|Ipv6Gateway.RatePercentageOutToInternet|userId and instanceId|Value|

