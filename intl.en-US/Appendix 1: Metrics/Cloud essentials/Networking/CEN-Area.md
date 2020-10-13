# CEN-Area

This topic describes the metrics for Cloud Enterprise Network \(CEN\) across areas.

-   Set the **Namespace** parameter to **acs\_cen**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Area Internet Out Rate|bit/s|InternetOutRateByConnectionArea|userId, cenId, geographicSpanId, and bandwidthPackageId|Value|
|Area Internet Out Rate Percent|%|InternetOutRatePercentByConnectionArea|userId, cenId, geographicSpanId, and bandwidthPackageId|Value|

