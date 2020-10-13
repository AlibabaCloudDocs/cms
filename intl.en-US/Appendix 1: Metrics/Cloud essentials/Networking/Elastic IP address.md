# Elastic IP address

This topic describes the metrics for Elastic IP addresses \(EIPs\).

-   Set the **Namespace** parameter to **acs\_vpc\_eip**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Inbound Traffic|byte|net.rx|userld and instanceld|Average, Minimum, Maximum, Sum|
|Inbound Package Number|count|net.rxPkgs|userld and instanceld|Average, Minimum, Maximum, Sum|
|Outbound Traffic|byte|net.tx|userld and instanceld|Average, Minimum, Maximum, Sum|
|Outbound Package Number|count|net.txPkgs|userld and instanceld|Average, Minimum, Maximum, Sum|
|Inbound Bandwidth|bit/s|net\_rx.rate|userld and instanceld|Value|
|Inbound Packet Rate|packet/s|net\_rxPkgs.rate|userld and instanceld|Value|
|Outbound Bandwidth|bit/s|net\_tx.rate|userld and instanceld|Value|
|Outbound Packet Rate|packet/s|net\_txPkgs.rate|userld and instanceld|Value|
|Out Ratelimit Drop Speed|packet/s|out\_ratelimit\_drop\_speed|userld and instanceld|Average|
|InternetInRatePercentage|%|net\_in.rate\_percentage|userld and instanceld|Average, Minimum, and Maximum|
|InternetOutRatePercentage|%|net\_out.rate\_percentage|userld and instanceld|Average, Minimum, and Maximum|

