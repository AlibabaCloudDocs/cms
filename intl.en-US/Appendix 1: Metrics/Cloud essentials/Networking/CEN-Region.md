# CEN-Region

This topic describes the metrics for Cloud Enterprise Network \(CEN\) across regions.

-   Set the **Namespace** parameter to **acs\_cen**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Region Internet Out Rate|Mbit/s|InternetOutRateByConnectionRegion|userId, cenId, geographicSpanId, localRegionId, and oppositeRegionId|Value|
|Region Internet Out Rate Percent|%|InternetOutRatePercentByConnectionRegion|userId, cenId, geographicSpanId, localRegionId, and oppositeRegionId|Value|
|InterRegion Packets Drop Rate|packet/s|InternetOutDropRateByConnectionRegion|userId, cenId, geographicSpanId, localRegionId, and oppositeRegionId|Average, Maximum, and Minimum|

