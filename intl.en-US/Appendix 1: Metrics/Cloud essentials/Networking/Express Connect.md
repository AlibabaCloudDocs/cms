# Express Connect

This topic describes the metrics for Express Connect.

-   Set the **Namespace** parameter to **acs\_express\_connect**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Intranet Inbound Traffic|byte|IntranetRX|userId and instanceId|Value|
|Intranet Outbound Traffic|byte|IntranetTX|userId and instanceId|Value|
|Inbound Bandwidth|bit/s|ReceiveBandwidth|userId and instanceId|Value|
|RouterInterfaceLossRate|%|RouterInterfaceLossRate|userId and instanceId|Maximum|
|RouterInterfaceResponseTime|ms|RouterInterfaceResponseTime|userId and instanceId|Maximum|
|Outbound Bandwidth|bit/s|TransportedBandwidth|userId and instanceId|Value|

