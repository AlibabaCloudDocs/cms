# NAT Gateway Bandwidth Package

This topic describes the metrics for the bandwidth plan feature of NAT Gateway.

-   Set the **Namespace** parameter to **acs\_nat\_gateway**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|Inbound Packet Rate|Count/Second|net\_rx.Pkgs|userId and instanceId|Value|
|Inbound Bandwidth|bits/s|net\_rx.rate|userId and instanceId|Value|
|Outbound Packet Rate|Count/Second|net\_tx.Pkgs|userId and instanceId|Value|
|Outbound Bandwidth|bits/s|net\_tx.rate|userId and instanceId|Value|
|Outbound Bandwidth Usage|%|net\_tx.ratePercent|userId and instanceId|Value|

