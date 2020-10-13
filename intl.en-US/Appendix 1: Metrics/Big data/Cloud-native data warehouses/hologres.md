# hologres

This topic describes the metrics for Hologres.

-   Set the **Namespace** parameter to **acs\_hologres**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|connections number|count|connection\_num|userId and instanceId|Average|
|cpu usage|%|cpu\_usage|userId and instanceId|Average|
|Delete SQL QPS|count/s|delete\_qps|userId and instanceId|Average|
|failed queries per second|count/s|failed\_queries|userId and instanceId|Average|
|Insert SQL QPS|count/s|insert\_qps|userId and instanceId|Average|
|memory usage|%|memory\_usage|userId and instanceId|Average|
|records\_per\_second|count/s|records\_per\_second|userId and instanceId|Average|
|select\_latency|s|select\_latency|userId and instanceId|Maximum|
|select latency p95|s|select\_latency\_p95|userId and instanceId|Maximum|
|select latency p999|s|select\_latency\_p999|userId and instanceId|Maximum|
|Select SQL QPS|count/s|select\_qps|userId and instanceId|Average|
|storage usage percent|%|storage\_usage\_percent|userId and instanceId|Average|
|Update SQL QPS|count/s|update\_qps|userId and instanceId|Average|
|storage\_usage|MB|storage\_usage|userId and instanceId|Average|

