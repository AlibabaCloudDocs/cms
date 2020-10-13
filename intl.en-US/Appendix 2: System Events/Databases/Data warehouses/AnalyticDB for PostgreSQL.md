# AnalyticDB for PostgreSQL

This topic describes the system events for AnalyticDB for PostgreSQL.

|Type|Event|Description|Status|Level|
|----|-----|-----------|------|-----|
|Exception|ComputeGroupCpuHigh|The CPU usage of a compute group exceeds 90%.|Failed|Critical|
|Exception|ComputeGroupMemoryHigh|The memory usage of a compute group exceeds 85%.|Failed|Critical|
|Exception|HighCoumputeGroupDiskUsed|The disk usage of a compute group exceeds 80%.|Failed|Critical|
|Exception|InstanceDown|The instance is unavailable.|Failed|Critical|
|Exception|LongTransaction|The number of long-running transactions is greater than or equal to 5.|Failed|Critical|
|Exception|MasterCpuHigh|The CPU usage of the master node exceeds 90%.|Failed|Critical|
|Exception|MasterMemoryHigh|The memory usage of the master node exceeds 85%.|Failed|Critical|
|Exception|NonSuperConnection|The proportion of connections with an instance exceeds 80%.|Failed|Critical|

