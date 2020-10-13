# Cloud Storage Gateway

This topic describes the metrics for Cloud Storage Gateway \(CSG\).

-   Set the **Namespace** parameter to **acs\_hcs\_sgw**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|file gateway share cache usage|%|cache\_used\_percent|userId, gatewayId, and share|Average|
|Host.cpu.user|%|cpu\_user|userId and gatewayId|Average|
|gateway memory usage|%|mem\_used\_percent|userId and gatewayId|Average|
|file gateway share meta disk usage|%|meta\_used\_percent|userId, gatewayId, and share|Average|
|file gateway share read write rate|KbyteSecond|rw\_rate|userId, gatewayId, and share|Average|
|file gateway share throttling status|state|throttling|userId, gatewayId, and share|Average|
|file gateway share upload rate|KByteSecond|upload\_rate|userId, gatewayId, and share|Average|
|block gateway volume cache usage|%|vol\_cache\_used\_percent|userId and gatewayId|Average|

