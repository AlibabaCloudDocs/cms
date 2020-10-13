# MaxCompute\_ subscription

This topic describes the metrics for subscription resources of quota groups in MaxCompute.

-   Set the **Namespace** parameter to **acs\_maxcompute\_prepay**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|pre-paid quota group cpu usage|%|PrePayQuotaGroupCPUUsed|userId and groupName|Average|
|QuotaGroupJobWaitQueue|count|PrePayQuotaGroupJobWaitQueue|userId and groupName|Value|
|pre-paid quota group mem usage|MB|PrePayQuotaGroupMemUsed|userId and groupName|Average|

