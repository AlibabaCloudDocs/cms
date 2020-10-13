# OpenSearch

This topic describes the metrics for Open Search.

-   Set the **Namespace** parameter to **acs\_opensearch**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|ComputeCostbyApp|LCU|ComputeCostbyApp|userId, regionId, appName, and appId|Average and Maximum|
|ComputeResourceRatiobyApp|%|computeResourceRatiobyApp|userId, regionId, appName, and appId|Maximum|
|ComputeResourcebyApp|LCU|ComputeResourcebyApp|userId, regionId, appName, and appId|Maximum|
|DailyPeakComputeResourcebyApp|LCU|DailyPeakComputeResourcebyApp|userId, regionId, appName, and appId|Maximum|
|DocCount|Count|DocCountbyApp|userId, regionId, appName, and appId|Maximum|
|DocSizeRatio|%|DocSizeRatiobyApp|userId, regionId, appName, and appId|Maximum|
|DocSizebyApp|Bytes|DocSizebyApp|userId, regionId, appName, and appId|Maximum|
|LatencybyApp|ms|LatencybyApp|userId, regionId, appName, and appId|Average and Maximum|
|LossQPS|Count/Second|LossQPSbyApp|userId, regionId, appName, and appId|Average and Maximum|
|QPS|Count/Second|QPSbyApp|userId, regionId, appName, and appId|Average and Maximum|
|APP Realtime Trigger Latency|ms|app\_realtime\_trigger\_latency|userId, regionId, appName, and appId|Average|
|APP Realtime Write Latency|ms|app\_realtime\_write\_latency|userId, regionId, appName, and appId|Maximum|
|app\_write\_rate\_limit\_qps|Count/s|app\_write\_rate\_limit\_qps|userId, regionId, appName, and appId|Average|

