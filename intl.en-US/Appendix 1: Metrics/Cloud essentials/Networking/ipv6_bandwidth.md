# ipv6\_bandwidth

This topic describes the metrics for IPV6 Internet bandwidth.

-   Set the **Namespace** parameter to **acs\_ipv6\_bandwidth**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|PkgsInFromInternet|pps|Ipv6Address.PkgsInFromInternet|userId and instanceId|Value|
|PkgsOutToInternet|pps|Ipv6Address.PkgsOutToInternet|userId and instanceId|Value|
|RateDropInFromInternet|pps|Ipv6Address.RateDropInFromInternet|userId and instanceId|Value|
|RateDropInFromInternet|pps|Ipv6Address.RateDropOutFromInternet|userId and instanceId|Value|
|RateInFromInternet|bits/s|Ipv6Address.RateInFromInternet|userId and instanceId|Value|
|RateLimitedPkgsDropInFromInternet|pps|Ipv6Address.RateLimitedPkgsDropInFromInternet|userId and instanceId|Value|
|RateLimitedPkgsDropOutToInternet|pps|Ipv6Address.RateLimitedPkgsDropOutToInternet|userId and instanceId|Value|
|RateOutToInternet|bits/s|Ipv6Address.RateOutToInternet|userId and instanceId|Value|
|Public Network Inbound Traffic Percentage|Value|Ipv6Address.RatePercentageInFromInternet|userId and instanceId|Value|
|Public Network Outbound Traffic Percent|Value|Ipv6Address.RatePercentageOutToInternet|userId and instanceId|Value|

