# MaxCompute\_ subscription

This topic describes the metrics for subscription resources of users in MaxCompute.

-   Set the **Namespace** parameter to **acs\_maxcompute\_prepay**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|pre-paid quota group cpu usage in each region|%|UserRegionQGCPUUtilization|userId and regionId|Average|
|pre-paid quota group memory usage in each region|%|UserRegionQGMEMUtilization|userId and regionId|Average|

