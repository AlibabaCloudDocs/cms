# enhanced\_nat\_gateway

This topic describes the metrics for enhanced NAT Gateway.

-   Set the **Namespace** parameter to **acs\_nat\_gateway**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|BWRateInFromInside|bps|BWRateInFromInside|userId and instanceId|Value|
|BWRateInFromOutside|bps|BWRateInFromOutside|userId and instanceId|Value|
|BWRateOutToInside|bps|BWRateOutToInside|userId and instanceId|Value|
|BWRateOutToOutside|bps|BWRateOutToOutside|userId and instanceId|Value|
|BytesInFromInside|bytes|BytesInFromInside|userId and instanceId|Value|
|BytesInFromOutside|bytes|BytesInFromOutside|userId and instanceId|Value|
|BytesOutToInside|bytes|BytesOutToInside|userId and instanceId|Value|
|BytesOutToOutside|bytes|BytesOutToOutside|userId and instanceId|Value|
|PPSRateInFromInside|countS|PPSRateInFromInside|userId and instanceId|Value|
|PPSRateInFromOutside|countS|PPSRateInFromOutside|userId and instanceId|Value|
|PPSRateOutToInside|countS|PPSRateOutToInside|userId and instanceId|Value|
|PPSRateOutToOutside|countS|PPSRateOutToOutside|userId and instanceId|Value|
|PacketsInFromInside|count|PacketsInFromInside|userId and instanceId|Value|
|PacketsInFromOutside|count|PacketsInFromOutside|userId and instanceId|Value|
|PacketsOutToInside|count|PacketsOutToInside|userId and instanceId|Value|
|PacketsOutToOutside|count|PacketsOutToOutside|userId and instanceId|Value|
|SessionActiveConnection|count|SessionActiveConnection|userId and instanceId|Value|
|SessionActiveConnectionWaterLever|%|SessionActiveConnectionWaterLever|userId and instanceId|Value|
|SessionLimitDropConnection|countS|SessionLimitDropConnection|userId and instanceId|Value|
|SessionNewConnection|countS|SessionNewConnection|userId and instanceId|Value|
|SessionNewConnectionWaterLever|%|SessionNewConnectionWaterLever|userId and instanceId|Value|
|SessionNewLimitDropConnection|countS|SessionNewLimitDropConnection|userId and instanceId|Value|

