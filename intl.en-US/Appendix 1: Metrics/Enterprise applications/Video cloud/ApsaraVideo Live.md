# ApsaraVideo Live

This topic describes the metrics for ApsaraVideo Live.

-   Set the **Namespace** parameter to **acs\_videolive**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|QPS|count/s|QPS|userId and instanceId|Average, Maximum, and Minimum|
|4xx Code|%|code4xx|userId and instanceId|Average, Maximum, and Minimum|
|5xx Code|%|code5xx|userId and instanceId|Average, Maximum, and Minimum|

