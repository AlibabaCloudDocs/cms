# OpenSearch

通过本文您可以了解开放搜索（OpenSearch）的监控项。

-   **Namespace**为**acs\_opensearch**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|单次查询计算消耗|LCU|ComputeCostbyApp|userId、regionId、appName、appId|Average、Maximum|
|计算资源使用率|%|computeResourceRatiobyApp|userId、regionId、appName、appId|Maximum|
|计算资源|LCU|ComputeResourcebyApp|userId、regionId、appName、appId|Maximum|
|DailyPeakComputeResourcebyApp|LCU|DailyPeakComputeResourcebyApp|userId、regionId、appName、appId|Maximum|
|文档总数|Count|DocCountbyApp|userId、regionId、appName、appId|Maximum|
|存储容量使用率|%|DocSizeRatiobyApp|userId、regionId、appName、appId|Maximum|
|存储容量|Bytes|DocSizebyApp|userId、regionId、appName、appId|Maximum|
|查询耗时|ms|LatencybyApp|userId、regionId、appName、appId|Average、Maximum|
|查询限流QPS|Count/Second|LossQPSbyApp|userId、regionId、appName、appId|Average、Maximum|
|查询QPS|Count/Second|QPSbyApp|userId、regionId、appName、appId|Average、Maximum|
|应用附表处理延迟|ms|app\_realtime\_trigger\_latency|userId、regionId、appName、appId|Average|
|应用实时处理延迟|ms|app\_realtime\_write\_latency|userId、regionId、appName、appId|Maximum|
|应用实时推送限速QPS|Count/s|app\_write\_rate\_limit\_qps|userId、regionId、appName、appId|Average|

