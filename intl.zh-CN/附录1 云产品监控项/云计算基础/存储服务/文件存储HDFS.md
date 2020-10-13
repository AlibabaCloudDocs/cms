# 文件存储HDFS

通过本文您可以了解文件存储HDFS的监控项。

-   **Namespace**为**acs\_hdfs**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|文件系统读请求频率|Count/Second|read\_iops|userId、instanceId|Average|
|文件系统读取请求大小|Byte|read\_iosize|userId、instanceId|Average|
|文件系统每秒读取字节数|Byte/s|read\_throughput|userId、instanceId|Average|
|文件系统空间剩余量|Byte|remaining\_storagespace|userId、instanceId|Average|
|文件系统空间使用率|%|storageutilization|userId、instanceId|Average|
|文件系统空间使用量|Byte|used\_storagespace|userId、instanceId|Average|
|文件系统写请求频率|Count/Second|write\_iops|userId、instanceId|Average|
|文件系统写入请求大小|Byte|write\_iosize|userId、instanceId|Average|
|文件系统每秒写入字节数|Byte/s|write\_throughput|userId、instanceId|Average|

