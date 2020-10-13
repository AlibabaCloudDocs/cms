# MaxCompute\_PayAsYouGo

This topic describes the metrics for pay-as-you-go resources of MaxCompute.

-   Set the **Namespace** parameter to **acs\_maxcompute\_prepay**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Post-paid task daily consumption|CNY|TaskDailyCost|userId and project|Maximum|
|Post-paid task monthly consumption|CNY|TaskMonthlyCost|userId and project|Maximum|

