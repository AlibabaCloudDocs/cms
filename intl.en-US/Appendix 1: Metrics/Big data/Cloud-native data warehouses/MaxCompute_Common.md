# MaxCompute\_Common

This topic describes the metrics for MaxCompute.

-   Set the **Namespace** parameter to **acs\_maxcompute\_prepay**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Tunnel download datasize daily by project|MB|TunnelDownloadDatasizeDailyBP|userId and project|Maximum|
|Tunnel download traffic by project|byte/min|TunnelDownloadTrafficBP|userId and project|Average|
|Tunnel upload datasize daily by project|MB|TunnelUploadDatasizeDailyBP|userId and project|Average|
|Tunnel upload traffic by project|byte/min|TunnelUploadTrafficBP|userId and project|Average|

