# RDS-PostgreSQL

This topic describes the metrics for ApsaraDB RDS for PostgreSQL instances with disks.

-   Set the **Namespace** parameter to **acs\_rds\_dashboard**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|PG\_ActiveConnectionsPerCpu|count|active\_connections\_per\_cpu|userId and instanceId|Average|
|PG\_ConnectionsUtilization|%|conn\_usgae|userId and instanceId|Average|
|PG\_CPUUtilization|%|cpu\_usage|userId and instanceId|Average|
|PG\_IOPSUtilization|%|iops\_usage|userId and instanceId|Average|
|PG\_INODEUtilization|%|local\_fs\_inode\_usage|userId and instanceId|Average|
|PG\_DISKUtilization|%|local\_fs\_size\_usage|userId and instanceId|Average|
|PG\_MemoryUtilization|%|mem\_usage|userId and instanceId|Average|
|PG\_RO\_ReadLag|s|PG\_RO\_ReadLag|userId and instanceId|Average|
|PG\_RO\_StreamingStatus|value|PG\_RO\_StreamingStatus|userId and instanceId|Average|

