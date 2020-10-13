# Clickhouse

This topic describes the metrics for ApsaraDB for ClickHouse.

-   Set the **Namespace** parameter to **acs\_clickhouse**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|conn\_usage|%|conn\_usage|uid and logic\_name|Average|
|conn\_usage\_count|count|conn\_usage\_count|uid and logic\_name|Average|
|cpu\_usage|%|cpu\_usage|uid and logic\_name|Average|
|disk\_usage|%|disk\_usage|uid and logic\_name|Average|
|disk\_usage\_size|MB|disk\_usage\_size|uid and logic\_name|Average|
|insert\_mb\_ps|MB|insert\_mb\_ps|uid and logic\_name|Average|
|insert\_rows\_ps|count|insert\_rows\_ps|uid and logic\_name|Average|
|mem\_usage|%|mem\_usage|uid and logic\_name|Average|
|mem\_usage\_size|MB|mem\_usage\_size|uid and logic\_name|Average|
|qps|count/s|qps|uid and logic\_name|Average|

