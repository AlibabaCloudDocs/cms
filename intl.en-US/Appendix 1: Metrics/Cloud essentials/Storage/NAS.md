# NAS

This topic describes the metrics for Apsara File Storage NAS.

-   Set the **Namespace** parameter to **acs\_nas**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Read IOPS|count/s|IopsRead|userId and fileSystemId|Value|
|Write IOPS|count/s|IopsWrite|userId and fileSystemId|Value|
|Read Latency|ms|LatencyRead|userId and fileSystemId|Value|
|Write Latency|ms|LatencyWrite|userId and fileSystemId|Value|
|Metadata QPS|count/s|QpsMeta|userId and fileSystemId|Value|
|Read Throughput|MB/s|ThruputRead|userId and fileSystemId|Value|
|Write Throughput|MB/s|ThruputWrite|userId and fileSystemId|Value|

