# Express Connect

This topic describes the metrics of Express Connect.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_express\_connect**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|PkgsRateLimitDropOut|pps|RateLimitDropPps|userId and instanceId|Value|
|Inbound Bandwidth|bits/s|ReceiveBandwidth|userId and instanceId|Value|
|RouterInterfaceLossRate|%|RouterInterfaceLossRate|userId and instanceId|Maximum|
|RouterInterfaceResponseTime|ms|RouterInterfaceResponseTime|userId and instanceId|Maximum|
|Outbound Bandwidth|bits/s|TransportedBandwidth|userId and instanceId|Value|

