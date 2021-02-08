# NAT Gateway

This topic describes the metrics for NAT Gateway.

-   Set the **Namespace** parameter to **acs\_nat\_gateway**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|SNAT Connections|count/min|SnatConnection|userId and instanceId|Maximum|
|Capacity Limit discarded connections|count/min|SnatConnectionDrop\_ConcurrentConnectionLimit|userId and instanceId|Maximum|
|Speed limit discarded connections|count/min|SnatConnectionDrop\_ConnectionRateLimit|userId and instanceId|Maximum|
|NormalSessionLimitDropRate|count/s|SessionLimitDropRate|userId and instanceId|Value|
|NormalSessionNewLimitDropRate|count/s|SessionNewLimitDropRate|userId and instanceId|Value|
|NormalSessionNewConnection|count/s|SessionNewConnection2|userId and instanceId|Value|

