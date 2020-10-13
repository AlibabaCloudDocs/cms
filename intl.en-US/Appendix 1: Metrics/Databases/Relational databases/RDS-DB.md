# RDS-DB

This topic describes the metrics for ApsaraDB for RDS.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for ApsaraDB for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_rds\_dashboard**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

**Note:** Among ApsaraDB RDS for SQL Server instances, only the instances whose SQL Server version is 2008 R2 support the ConnectionsUtilization and MemoryUtilization metrics.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|ConnectionsUtilization|%|ConnectionUsage|userId and instanceId|Maximum, Minimum, and Average|
|CPU Usage|%|CpuUsage|userId and instanceId|Maximum, Minimum, and Average|
|DataDelay|s|DataDelay|userId and instanceId|Maximum, Minimum, and Average|
|DiskUtilization|%|DiskUsage|userId and instanceId|Maximum, Minimum, and Average|
|IOPSUtilization|%|IOPSUsage|userId and instanceId|Maximum, Minimum, and Average|
|MemoryUtilization|%|MemoryUsage|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_ActiveSessions|count|MySQL\_ActiveSessions|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_ComDelete|count/s|MySQL\_ComDelete|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_ComInsert|count/s|MySQL\_ComInsert|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_ComInsertSelect|count/s|MySQL\_ComInsertSelect|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_ComReplace|count/s|MySQL\_ComReplace|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_ComReplaceSelect|count/s|MySQL\_ComReplaceSelect|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_ComSelect|count/s|MySQL\_ComSelect|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_ComUpdate|count/s|MySQL\_ComUpdate|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_IbufRequestR|count/s|MySQL\_lbufRequestR|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_IbufRequestW|count/s|MySQL\_lbufRequestW|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_QPS|count/s|MySQL\_QPS|userId and instanceId|Maximum, Minimum, and Average|
|MySQL\_TPS|count/s|MySQL\_TPS|userId and instanceId|Maximum, Minimum, and Average|
|NetworkInRate|bit/s|SQLServer\_NetworkInNew|userId and instanceId|Maximum, Minimum, and Average|
|NetworkOutRate|bit/s|SQLServer\_NetworkOutNew|userId and instanceId|Maximum, Minimum, and Average|
|NetworkInRate|bits/s|MySQL\_NetworkInNew|userId and instanceId|Average, Minimum, and Maximum|
|NetworkOutRate|bits/s|MySQL\_NetworkOutNew|userId and instanceId|Average, Minimum, and Maximum|
|MySQL\_IbufDirtyRatio|%|MySQL\_IbufDirtyRatio|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_IbufUseRatio|%|MySQL\_IbufUseRatio|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_InnoDBDataRead|KB|MySQL\_InnoDBDataRead|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_InnoDBDataWritten|KB|MySQL\_InnoDBDataWritten|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_TempDiskTableCreates|count/s|MySQL\_TempDiskTableCreates|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_InnoDBRowUpdate|count/s|MySQL\_InnoDBRowUpdate|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_InnoDBRowInsert|count/s|MySQL\_InnoDBRowInsert|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_InnoDBRowDelete|count/s|MySQL\_InnoDBRowDelete|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_InnoDBRowRead|count/s|MySQL\_InnoDBRowRead|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_InnoDBLogFsync|count/s|MySQL\_InnoDBLogFsync|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_InnoDBLogWrites|count/s|MySQL\_InnoDBLogWrites|userId and instanceId|Average, Maximum, and Minimum|
|MySQL\_InnoDBLogWriteRequests|count/s|MySQL\_InnoDBLogWriteRequests|userId and instanceId|Average, Maximum, and Minimum|

