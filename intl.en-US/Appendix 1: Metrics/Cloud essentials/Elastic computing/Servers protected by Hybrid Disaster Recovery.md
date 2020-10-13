# Servers protected by Hybrid Disaster Recovery

This topic describes the metrics for servers protected by Hybrid Disaster Recovery \(HDR\).

-   Set the **Namespace** parameter to **acs\_hdr**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|server rpo|s|server\_info\_server.rpo|userId and serverId|Average|

