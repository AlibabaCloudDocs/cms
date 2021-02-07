# Clickhouse

This topic describes the metrics for ClickHouse.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_clickhouse**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|conn\_usage|%|conn\_usage|uid and logic\_name|Average|
|conn\_usage\_count|count|conn\_usage\_count|uid and logic\_name|Average|
|cpu\_usage|%|cpu\_usage|uid and logic\_name|Average|
|disk\_usage|%|disk\_usage|uid and logic\_name|Average|
|disk\_usage\_size|MB|disk\_usage\_size|uid and logic\_name|Average|
|insert\_mb\_ps|MB|insert\_mb\_ps|uid and logic\_name|Average|
|insert\_rows\_ps|line|insert\_rows\_ps|uid and logic\_name|Average|
|mem\_usage|%|mem\_usage|uid and logic\_name|Average|
|mem\_usage\_size|MB|mem\_usage\_size|uid and logic\_name|Average|
|qps|frequency|qps|uid and logic\_name|Average|

