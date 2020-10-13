# ApsaraDB Exclusive Host Group

This topic describes the metrics for the dedicated host group feature of ApsaraDB for RDS.

-   Set the **Namespace** parameter to **acs\_rds\_sar**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|MetricName|Metric|Unit|Dimensions|Statistics|
|----------|------|----|----------|----------|
|CPUUtilization|CPUUtilization|%|userId, hostGroupId, and hostId|Average|
|DiskReadIOPS|DiskReadIOPS|count/s|userId, hostGroupId, and hostId|Average|
|DiskWriteIOPS|DiskWriteIOPS|count/s|userId, hostGroupId, and hostId|Average|
|InternetIn|InternetIn|byte|userId, hostGroupId, and hostId|Average|
|InternetOut|InternetOut|byte|userId, hostGroupId, and hostId|Average|
|IntranetIn|IntranetIn|byte|userId, hostGroupId, and hostId|Average|
|IntranetOut|IntranetOut|byte|userId, hostGroupId, and hostId|Average|
|cpu\_system|cpu\_system|%|userId, hostGroupId, and hostId|Average|
|cpu\_total|cpu\_total|%|userId, hostGroupId, and hostId|Average|
|cpu\_user|cpu\_user|%|userId, hostGroupId, and hostId|Average|
|disk\_readbytes|disk\_readbytes|byte/s|userId, hostGroupId, and hostId|Average|
|disk\_readiops|disk\_readiops|count/s|userId, hostGroupId, and hostId|Average|
|disk\_writebytes|disk\_writebytes|byte/s|userId, hostGroupId, and hostId|Average|
|disk\_writeiops|disk\_writeiops|count/s|userId, hostGroupId, and hostId|Average|
|diskusage\_free|diskusage\_free|byte|userId, hostGroupId, hostId, and device|Average|
|diskusage\_total|diskusage\_total|byte|userId, hostGroupId, hostId, and device|Average|
|diskusage\_used|diskusage\_used|byte|userId, hostGroupId, hostId, and device|Average|
|diskusage\_utilization|diskusage\_utilization|%|userId, hostGroupId, hostId, and device|Average|
|load\_15m|load\_15m|%|userId, hostGroupId, and hostId|Average|
|load\_1m|load\_1m|%|userId, hostGroupId, and hostId|Average|
|load\_5m|load\_5m|%|userId, hostGroupId, and hostId|Average|
|memory\_freespace|memory\_freespace|byte|userId, hostGroupId, and hostId|Average|
|memory\_totalspace|memory\_totalspace|byte|userId, hostGroupId, and hostId|Average|
|memory\_usedspace|memory\_usedspace|byte|userId, hostGroupId, and hostId|Average|

