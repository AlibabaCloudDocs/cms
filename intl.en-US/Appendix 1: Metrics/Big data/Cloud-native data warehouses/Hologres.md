# Hologres

This topic describes the metrics of Hologres.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_hologres**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|connection count|Count|connection\_count|userId, instanceId, and dbName|Average and Sum|
|total connections count|Count|connection\_num|userId and instanceId|Average|
|cpu usage|%|cpu\_usage|userId and instanceId|Average|
|delete statement QPS|CountSecond|delete\_qps|userId and instanceId|Average|
|delete query latency|MilliSeconds|delete\_query\_latency|userId and instanceId|Average and Maximum|
|deleted records per second|CountS|delete\_record\_qps|userId and instanceId|Average|
|failed queries count|Count|failed\_queries|userId and instanceId|Average|
|Insert Statement QPS|CountSecond|insert\_qps|userId and instanceId|Average|
|insert query latency|MilliSeconds|insert\_query\_latency|userId and instanceId|Average and Maximum|
|memory usage|%|memory\_usage|userId and instanceId|Average|
|Query Latency Detail|MilliSeconds|query\_latency|instanceId, userId, and cmdType|Average|
|Query QPS Detail|CountS|query\_qps|instanceId, userId, and cmdType|Average|
|realtime ingestion throughput|Bytes|realtime\_ingestion\_throughput|userId and instanceId|Average|
|realtime ingestion rps|CountS|record\_input\_qps|instanceId and userId|Average|
|inserted records per second|CountS|records\_per\_second|userId and instanceId|Average|
|select latency p99|Seconds|select\_latency|userId and instanceId|Maximum|
|select latency p95|Seconds|select\_latency\_p95|userId and instanceId|Maximum|
|select latency p999|Seconds|select\_latency\_p999|userId and instanceId|Maximum|
|Select Statement QPS|CountSecond|select\_qps|userId and instanceId|Average|
|select query latency|MilliSeconds|select\_query\_latency|instanceId and userId|Average|
|storage\_usage|Bytes|storage\_usage|userId and instanceId|Average|
|storage usage percent|%|storage\_usage\_percent|userId and instanceId|Average|
|Update Statement QPS|CountSecond|update\_qps|userId and instanceId|Average|
|update query latency|MilliSeconds|update\_query\_latency|userId and instanceId|Average and Maximum|
|updated records per second|CountS|update\_record\_qps|userId and instanceId|Average|

