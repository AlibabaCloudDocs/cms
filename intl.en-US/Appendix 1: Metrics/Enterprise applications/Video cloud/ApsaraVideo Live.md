# ApsaraVideo Live

This topic describes the metrics of ApsaraVideo Live.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_videolive**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Peak Bandwidth|bits/s|BPS|userId and instanceId|Average, Maximum, and Minimum|
|InternetOut|Bytes|InternetOut|userId and instanceId|Sum|
|QPS|Count|QPS|userId and instanceId|Average, Maximum, and Minimum|
|4xx Code|%|code4xx|userId and instanceId|Average, Maximum, and Minimum|
|5xx Code|%|code5xx|userId and instanceId|Average, Maximum, and Minimum|

