# Gateway of Hybrid Disaster Recovery

This topic describes the metrics for gateways of Hybrid Disaster Recovery \(HDR\).

-   Set the **Namespace** parameter to **acs\_hdr**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|gateway cpu usage idle|%|cpu\_usage\_idle|userId and gatewayId|Average|
|gateway memory usage|%|mem\_used\_percent|userId and gatewayId|Average|
|gateway inboud network traffic|byte|net\_bytes\_recv|userId, gatewayId, and interface|Maximum|
|gateway outboud network traffic|byte|net\_bytes\_sent|userId, gatewayId, and interface|Maximum|

