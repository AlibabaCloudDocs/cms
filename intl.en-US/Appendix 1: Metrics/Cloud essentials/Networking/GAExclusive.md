# GAExclusive

This topic describes the metrics for dedicated-bandwidth Global Accelerator instances.

-   Set the **Namespace** parameter to **acs\_global\_acceleration**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|Inbound Data Package|pps|InternetInPPS|userId and instanceId|Value|
|Network Inflow Bandwidth|bits/s|InternetInRate|userId and instanceId|Value|
|Outbound Data Package|pps|InternetOutPPS|userId and instanceId|Value|
|Outbound Bandwidth|bits/s|InternetOutRate|userId and instanceId|Value|

