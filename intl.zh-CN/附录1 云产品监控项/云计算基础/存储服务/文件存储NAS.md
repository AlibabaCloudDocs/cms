# 文件存储NAS

通过本文您可以了解文件存储NAS的监控项。

-   **Namespace**为**acs\_nas**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|读IOPS|op/s|IopsRead|userId、fileSystemId|Value|
|写IOPS|op/s|IopsWrite|userId、fileSystemId|Value|
|读延迟|ms|LatencyRead|userId、fileSystemId|Value|
|写延迟|ms|LatencyWrite|userId、fileSystemId|Value|
|元数据QPS|op/s|QpsMeta|userId、fileSystemId|Value|
|读吞吐|MB/s|ThruputRead|userId、fileSystemId|Value|
|写吞吐|MB/s|ThruputWrite|userId、fileSystemId|Value|

