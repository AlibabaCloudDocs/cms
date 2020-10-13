# CEN-Router

This topic describes the metrics for the border router feature of Cloud Enterprise Network \(CEN\).

-   Set the **Namespace** parameter to **acs\_cen**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|Healthy Check Latency|ms|VBRHealthyCheckLatency|userId, cenId, and vbrInstanceId|Value|
|Healthy Check Loss Rate|%|VBRHealthyCheckLossRate|userId, cenId, and vbrInstanceId|Value|
|Internet In Rate|bits/s|VBRInternetInRate|userId, cenId, and vbrInstanceId|Value|
|Internet Out Rate|bits/s|VBRInternetOutRate|userId, cenId, and vbrInstanceId|Value|

