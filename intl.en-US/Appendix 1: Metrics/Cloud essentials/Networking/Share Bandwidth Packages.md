# Share Bandwidth Packages

This topic describes the metrics for Internet Shared Bandwidth.

-   Set the **Namespace** parameter to **acs\_bandwidth\_package**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|Inbound Packet Rate|pps|net\_rx.Pkgs|userId and instanceId|Value|
|Inbound Bandwidth|bits/s|net\_rx.rate|userId and instanceId|Value|
|Outbound Packet Rate|pps|net\_tx.Pkgs|userId and instanceId|Value|
|Outbound Bandwidth|bits/s|net\_tx.rate|userId and instanceId|Value|
|Outbound Bandwidth Usage|%|net\_tx.ratePercent|userId and instanceId|Value|

