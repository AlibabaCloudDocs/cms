# ApsaraDB for MongoDB-Instance Copy

This topic describes the metrics of ApsaraDB for MongoDB of the replica set architecture.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_mongodb**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|\(Host&Slave\) CPU Usage|%|CPUUtilization|userId, instanceId, and role|Maximum, Minimum, and Average|
|\(Host&Slave\) Connection Usage|Count|ConnectionAmount|userId, instanceId, and role|Maximum, Minimum, and Average|
|\(Host&Slave\) Connection Usage|%|ConnectionUtilization|userId, instanceId, and role|Maximum, Minimum, and Average|
|\(Host&Slave\) Disk Size Occupied by Data|Byte|DataDiskAmount|userId, instanceId, and role|Maximum, Minimum, and Average|
|\(Host&Slave\) Disk Usage|%|DiskUtilization|userId, instanceId, and role|Maximum, Minimum, and Average|
|\(Host&Slave\) IOPS Usage|%|IOPSUtilization|userId, instanceId, and role|Maximum, Minimum, and Average|
|\(Host&Slave\) Disk Size Occupied by Instances|Byte|InstanceDiskAmount|userId, instanceId, and role|Maximum, Minimum, and Average|
|\(Host&Slave\) Cache Inbound Bandwidth|Byte|IntranetIn|userId, instanceId, and role|Maximum, Minimum, and Average|
|\(Host&Slave\) Cache Outbound Bandwidth|Byte|IntranetOut|userId, instanceId, and role|Maximum, Minimum, and Average|
|\(Host&Slave\) Disk Size Occupied by Logs|Byte|LogDiskAmount|userId, instanceId, and role|Maximum, Minimum, and Average|
|\(Host&Slave\) Memory Usage|%|MemoryUtilization|userId, instanceId, and role|Maximum, Minimum, and Average|
|\(Host&Slave\) Number of Requests|Count|NumberRequests|userId, instanceId, and role|Maximum, Minimum, and Average|
|\(Host&Slave\) Number of Command Operations|Frequency|OpCommand|userId, instanceId, and role|Maximum, Minimum, and Average|
|\(Host&Slave\) Number of Delete Operations|Frequency|OpDelete|userId, instanceId, and role|Maximum, Minimum, and Average|
|\(Host&Slave\) Number of Getmore Operations|Frequency|OpGetmore|userId, instanceId, and role|Maximum, Minimum, and Average|
|\(Host&Slave\) Number of Insert Operations|Count|OpInsert|userId, instanceId, and role|Maximum, Minimum, and Average|
|\(Host&Slave\) Number of Query Operations|Frequency|OpQuery|userId, instanceId, and role|Maximum, Minimum, and Average|
|\(Host&Slave\) Number of Update Operations|Frequency|OpUpdate|userId, instanceId, and role|Maximum, Minimum, and Average|
|\(Host&Slave\) QPS|Count|QPS|userId, instanceId, and role|Maximum, Minimum, and Average|

