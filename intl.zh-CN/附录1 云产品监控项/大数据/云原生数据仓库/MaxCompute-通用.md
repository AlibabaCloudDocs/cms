# MaxCompute-通用

通过本文您可以了解大数据计算服务MaxCompute的通用版的监控项。

-   **Namespace**为**acs\_maxcompute\_prepay**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|Tunnel日累计下载数据量\_project级别|MB|TunnelDownloadDatasizeDailyBP|userId、project|Maximum|
|Tunnel下载流量\_project级别|bytes/minute|TunnelDownloadTrafficBP|userId、project|Average|
|Tunnel日累计上传数据量\_project级别|MB|TunnelUploadDatasizeDailyBP|userId、project|Average|
|Tunnel上传流量\_project级别|bytes/minute|TunnelUploadTrafficBP|userId、project|Average|

