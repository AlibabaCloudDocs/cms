# RDS-DB

This topic describes the metrics of ApsaraDB RDS.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_rds\_dashboard**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

**Note:** Only Microsoft SQL Server instances of the 2008 R2 version support the ConnectionsUtilization and MemoryUtilization metrics.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|ConnectionUsage|%|ConnectionUsage|userId and instanceId|Maximum, Minimum, and Average|
|CPU Usage|%|CpuUsage|userId and instanceId|Maximum, Minimum, and Average|
|DataDelay|Second|DataDelay|userId and instanceId|Maximum, Minimum, and Average|
|DiskUtilization|%|DiskUsage|userId and instanceId|Maximum, Minimum, and Average|
|IOPSUtilization|%|IOPSUsage|userId and instanceId|Maximum, Minimum, and Average|
|MemoryUtilization|%|MemoryUsage|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_ActiveSessions|count|MySQL\_ActiveSessions|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_ComDelete|countSecond|MySQL\_ComDelete|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_ComInsert|countSecond|MySQL\_ComInsert|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_ComInsertSelect|countSecond|MySQL\_ComInsertSelect|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_ComReplace|countSecond|MySQL\_ComReplace|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_ComReplaceSelect|countSecond|MySQL\_ComReplaceSelect|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_ComSelect|countSecond|MySQL\_ComSelect|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_ComUpdate|countSecond|MySQL\_ComUpdate|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_IbufRequestR|countSecond|MySQL\_lbufRequestR|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_IbufRequestW|countSecond|MySQL\_lbufRequestW|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_QPS|countSecond|MySQL\_QPS|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_TPS|countSecond|MySQL\_TPS|userId and instanceId|Maximum, Minimum, and Average|
|NetworkInRate|bit/s|SQLServer\_NetworkInNew|userId and instanceId|Maximum, Minimum, and Average|
|NetworkOutRate|bit/s|SQLServer\_NetworkOutNew|userId and instanceId|Maximum, Minimum, and Average|
|NetworkInRate|bits/s|MySQL\_NetworkInNew|userId and instanceId|Average, Minimum, and Maximum|
|NetworkOutRate|bits/s|MySQL\_NetworkOutNew|userId and instanceId|Average, Minimum, and Maximum|
|MySQL\_IbufDirtyRatio|%|MySQL\_IbufDirtyRatio|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_IbufUseRatio|%|MySQL\_IbufUseRatio|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_InnoDBDataRead|Kbyte|MySQL\_InnoDBDataRead|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_InnoDBDataWritten|Kbyte|MySQL\_InnoDBDataWritten|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_TempDiskTableCreates|countSecond|MySQL\_TempDiskTableCreates|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_InnoDBRowUpdate|countSecond|MySQL\_InnoDBRowUpdate|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_InnoDBRowInsert|countSecond|MySQL\_InnoDBRowInsert|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_InnoDBRowDelete|countSecond|MySQL\_InnoDBRowDelete|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_InnoDBRowRead|countSecond|MySQL\_InnoDBRowRead|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_InnoDBLogFsync|countSecond|MySQL\_InnoDBLogFsync|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_InnoDBLogWrites|countSecond|MySQL\_InnoDBLogWrites|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_InnoDBLogWriteRequests|countSecond|MySQL\_InnoDBLogWriteRequests|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_SlowQueries|countSecond|MySQL\_SlowQueries|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_IbufReadHit|%|MySQL\_IbufReadHit|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_ibufPoolReads|countSecond|MySQL\_ibufPoolReads|userId and instanceId|Average, Maximum, and Minimum|

