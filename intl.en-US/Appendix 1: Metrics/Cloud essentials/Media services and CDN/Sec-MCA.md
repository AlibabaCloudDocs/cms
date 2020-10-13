# Sec-MCA

This topic describes the metrics for Secure Content Delivery Network \(SCDN\).

-   Set the **Namespace** parameter to **acs\_scdn**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Peak Bandwidth|bit/s|BPS|userId and instanceId|Average|
|QPS|count/s|QPS|userId and instanceId|Average|
|4XX Return Code ratio|%|code4xx|userId and instanceId|Average|
|5XX Return Code ratio|%|code5xx|userId and instanceId|Average|
|Hit Rate|%|hitRate|userId and instanceId|Average|

