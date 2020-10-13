# 云数据库RDS版（RDS）

通过本文您可以了解云数据库RDS版的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_rds\_dashboard**。
-   **Period**默认为60秒，也可以为60的整数倍。

**说明：** 对于Microsoft SQL Server实例，只有2008 R2版本支持连接数使用率和内存使用率。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|连接数使用率|%|ConnectionUsage|userId、instanceId|Maximum、Minimum、Average|
|CPU使用率|%|CpuUsage|userId、instanceId|Maximum、Minimum、Average|
|只读实例延迟|Second|DataDelay|userId、instanceId|Maximum、Minimum、Average|
|磁盘使用率|%|DiskUsage|userId、instanceId|Maximum、Minimum、Average|
|IOPS使用率|%|IOPSUsage|userId、instanceId|Maximum、Minimum、Average|
|内存使用率|%|MemoryUsage|userId、instanceId|Maximum、Minimum、Average|
|MySQL\_ActiveSessions|count|MySQL\_ActiveSessions|userId、instanceId|Maximum、Minimum、Average|
|MySQL每秒Delete量|countSecond|MySQL\_ComDelete|userId、instanceId|Maximum、Minimum、Average|
|MySQL每秒Insert量|countSecond|MySQL\_ComInsert|userId、instanceId|Maximum、Minimum、Average|
|MySQL每秒InsertSelect量|countSecond|MySQL\_ComInsertSelect|userId、instanceId|Maximum、Minimum、Average|
|MySQL每秒Replace量|countSecond|MySQL\_ComReplace|userId、instanceId|Maximum、Minimum、Average|
|MySQL每秒ReplaceSelect量|countSecond|MySQL\_ComReplaceSelect|userId、instanceId|Maximum、Minimum、Average|
|MySQL每秒Select量|countSecond|MySQL\_ComSelect|userId、instanceId|Maximum、Minimum、Average|
|MySQL每秒Update量|countSecond|MySQL\_ComUpdate|userId、instanceId|Maximum、Minimum、Average|
|MySQL每秒逻辑读次数|countSecond|MySQL\_lbufRequestR|userId、instanceId|Maximum、Minimum、Average|
|MySQL每秒逻辑写次数|countSecond|MySQL\_lbufRequestW|userId、instanceId|Maximum、Minimum、Average|
|MySQL每秒查询量|countSecond|MySQL\_QPS|userId、instanceId|Maximum、Minimum、Average|
|MySQL每秒事务数|countSecond|MySQL\_TPS|userId、instanceId|Maximum、Minimum、Average|
|SQLServer网络流入带宽|bit/s|SQLServer\_NetworkInNew|userId、instanceId|Maximum、Minimum、Average|
|SQLServer网络流出带宽|bit/s|SQLServer\_NetworkOutNew|userId、instanceId|Maximum、Minimum、Average|
|MySQL网络流入带宽|bits/s|MySQL\_NetworkInNew|userId、instanceId|Average、Minimum、Maximum|
|MySQL网络流出带宽|bits/s|MySQL\_NetworkOutNew|userId、instanceId|Average、Minimum、Maximum|
|MySQL\_BP脏页百分率|%|MySQL\_IbufDirtyRatio|userId、instanceId|Average、Maximum、Minimum|
|MySQL\_BP利用率|%|MySQL\_IbufUseRatio|userId、instanceId|Average、Maximum、Minimum|
|MySQL\_InnoDB每秒读取数据量|Kbyte|MySQL\_InnoDBDataRead|userId、instanceId|Average、Maximum、Minimum|
|MySQL\_InnoDB每秒写入数据量|Kbyte|MySQL\_InnoDBDataWritten|userId、instanceId|Average、Maximum、Minimum|
|MySQL每秒创建临时表数量|countSecond|MySQL\_TempDiskTableCreates|userId、instanceId|Average、Maximum、Minimum|
|MySQL\_InnoDB每秒更新行数|countSecond|MySQL\_InnoDBRowUpdate|userId、instanceId|Average、Maximum、Minimum|
|MySQL\_InnoDB每秒插入行数|countSecond|MySQL\_InnoDBRowInsert|userId、instanceId|Average、Maximum、Minimum|
|MySQL\_InnoDB每秒删除行数|countSecond|MySQL\_InnoDBRowDelete|userId、instanceId|Average、Maximum、Minimum|
|MySQL\_InnoDB每秒读取行数|countSecond|MySQL\_InnoDBRowRead|userId、instanceId|Average、Maximum、Minimum|
|MySQL\_InnoDB每秒日志fsync量|countSecond|MySQL\_InnoDBLogFsync|userId、instanceId|Average、Maximum、Minimum|
|MySQL\_InnoDB每秒日志物理写次数|countSecond|MySQL\_InnoDBLogWrites|userId、instanceId|Average、Maximum、Minimum|
|MySQL\_InnoDB每秒日志写请求次数|countSecond|MySQL\_InnoDBLogWriteRequests|userId、instanceId|Average、Maximum、Minimum|

