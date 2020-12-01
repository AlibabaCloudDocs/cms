# ApsaraDB RDS

This topic describes the metrics of ApsaraDB RDS.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_rds\_dashboard**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

**Note:** Among ApsaraDB RDS for SQL Server instances with the Microsoft SQL Server database engine, only the instances whose SQL Server version is 2008 R2 support the ConnectionsUtilization and MemoryUtilization metrics.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|ConnectionsUtilization|%|ConnectionUsage|userId and instanceId|Maximum, Minimum, and Average|
|CPU Usage|%|CpuUsage|userId and instanceId|Maximum, Minimum, and Average|
|DataDelay|Second|DataDelay|userId and instanceId|Maximum, Minimum, and Average|
|DiskUtilization|%|DiskUsage|userId and instanceId|Maximum, Minimum, and Average|
|IOPSUtilization|%|IOPSUsage|userId and instanceId|Maximum, Minimum, and Average|
|MemoryUtilization|%|MemoryUsage|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_ActiveSessions|Count|MySQL\_ActiveSessions|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_ComDelete|CountSecond|MySQL\_ComDelete|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_ComInsert|CountSecond|MySQL\_ComInsert|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_ComInsertSelect|CountSecond|MySQL\_ComInsertSelect|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_ComReplace|CountSecond|MySQL\_ComReplace|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_ComReplaceSelect|CountSecond|MySQL\_ComReplaceSelect|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_ComSelect|CountSecond|MySQL\_ComSelect|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_ComUpdate|CountSecond|MySQL\_ComUpdate|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_IbufRequestR|CountSecond|MySQL\_lbufRequestR|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_IbufRequestW|CountSecond|MySQL\_lbufRequestW|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_QPS|CountSecond|MySQL\_QPS|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_TPS|CountSecond|MySQL\_TPS|userId and instanceId|Maximum, Minimum, and Average|
|NetworkInRate|bit/s|SQLServer\_NetworkInNew|userId and instanceId|Maximum, Minimum, and Average|
|NetworkOutRate|bit/s|SQLServer\_NetworkOutNew|userId and instanceId|Maximum, Minimum, and Average|
|NetworkInRate|bits/s|MySQL\_NetworkInNew|userId and instanceId|Average, Minimum, and Maximum|
|NetworkOutRate|bits/s|MySQL\_NetworkOutNew|userId and instanceId|Average, Minimum, and Maximum|
|MySQL\_IbufDirtyRatio|%|MySQL\_IbufDirtyRatio|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_IbufUseRatio|%|MySQL\_IbufUseRatio|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_InnoDBDataRead|KByte|MySQL\_InnoDBDataRead|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_InnoDBDataWritten|KByte|MySQL\_InnoDBDataWritten|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_TempDiskTableCreates|CountSecond|MySQL\_TempDiskTableCreates|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_InnoDBRowUpdate|CountSecond|MySQL\_InnoDBRowUpdate|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_InnoDBRowInsert|CountSecond|MySQL\_InnoDBRowInsert|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_InnoDBRowDelete|CountSecond|MySQL\_InnoDBRowDelete|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_InnoDBRowRead|CountSecond|MySQL\_InnoDBRowRead|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_InnoDBLogFsync|CountSecond|MySQL\_InnoDBLogFsync|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_InnoDBLogWrites|CountSecond|MySQL\_InnoDBLogWrites|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_InnoDBLogWriteRequests|CountSecond|MySQL\_InnoDBLogWriteRequests|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_SlowQueries|CountSecond|MySQL\_SlowQueries|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_IbufReadHit|%|MySQL\_IbufReadHit|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_ibufPoolReads|CountSecond|MySQL\_ibufPoolReads|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_DataDiskSize|MB|MySQL\_DataDiskSize|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_InstanceDiskSize|MB|MySQL\_InstanceDiskSize|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_LogDiskSize|MB|MySQL\_LogDiskSize|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_OtherDiskSize|MB|MySQL\_OtherDiskSize|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_TmpDiskSize|MB|MySQL\_TmpDiskSize|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_ProxyCpuUsage|%|MySQL\_ProxyCpuUsage|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_ProxyMemUsage|%|MySQL\_ProxyMemUsage|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_SlaveIORunning|Value|MySQL\_SlaveIORunning|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_SlaveSQLRunning|Value|MySQL\_SlaveSQLRunning|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_ThreadsConnected|Count|MySQL\_ThreadsConnected|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_ThreadsRunning|Count|MySQL\_ThreadsRunning|userId and instanceId|Average, Maximum, and Minimum|

