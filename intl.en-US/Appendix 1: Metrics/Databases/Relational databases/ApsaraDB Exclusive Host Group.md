# ApsaraDB Exclusive Host Group

This topic describes the metrics of the exclusive host group of ApsaraDB RDS.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_rds\_sar**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|CPUUtilization|%|CPUUtilization|userId, hostGroupId, and hostId|Average|
|DiskReadIOPS|CountSecond|DiskReadIOPS|userId, hostGroupId, and hostId|Average|
|DiskWriteIOPS|CountSecond|DiskWriteIOPS|userId, hostGroupId, and hostId|Average|
|InternetIn|MByte|InternetIn|userId, hostGroupId, and hostId|Average|
|InternetOut|MByte|InternetOut|userId, hostGroupId, and hostId|Average|
|IntranetIn|MByte|IntranetIn|userId, hostGroupId, and hostId|Average|
|IntranetOut|MByte|IntranetOut|userId, hostGroupId, and hostId|Average|
|cpu\_system|%|cpu\_system|userId, hostGroupId, and hostId|Average|
|cpu\_total|%|cpu\_total|userId, hostGroupId, and hostId|Average|
|cpu\_user|%|cpu\_user|userId, hostGroupId, and hostId|Average|
|disk\_readbytes|MByte/s|disk\_readBytes|userId, hostGroupId, and hostId|Average|
|disk\_readiops|CountSecond|disk\_readiops|userId, hostGroupId, and hostId|Average|
|disk\_writebytes|Byte/s|disk\_writeBytes|userId, hostGroupId, and hostId|Average|
|disk\_writeiops|CountSecond|disk\_writeiops|userId, hostGroupId, and hostId|Average|
|diskusage\_free|MByte|diskusage\_free|userId, hostGroupId, hostId, and device|Average|
|diskusage\_total|MByte|diskusage\_total|userId, hostGroupId, hostId, and device|Average|
|diskusage\_used|MByte|diskusage\_used|userId, hostGroupId, hostId, and device|Average|
|diskusage\_utilization|%|diskusage\_utilization|userId, hostGroupId, hostId, and device|Average|
|load\_15m|%|load\_15m|userId, hostGroupId, and hostId|Average|
|load\_1m|%|load\_1m|userId, hostGroupId, and hostId|Average|
|load\_5m|%|load\_5m|userId, hostGroupId, and hostId|Average|
|memory\_freespace|MByte|memory\_freespace|userId, hostGroupId, and hostId|Average|
|memory\_totalspace|MByte|memory\_totalspace|userId, hostGroupId, and hostId|Average|
|memory\_usedspace|MByte|memory\_usedspace|userId, hostGroupId, and hostId|Average|

