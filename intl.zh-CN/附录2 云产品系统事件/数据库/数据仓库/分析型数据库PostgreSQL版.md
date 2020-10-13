# 分析型数据库PostgreSQL版

通过本文您可以了解分析型数据库PostgreSQL版的系统事件。

|事件类型|事件名称|事件含义|事件状态|事件等级|
|----|----|----|----|----|
|Exception|ComputeGroupCpuHigh|计算组CPU水位超过90%|Failed|Critical|
|Exception|ComputeGroupMemoryHigh|计算组内存水位超过85%|Failed|Critical|
|Exception|HighCoumputeGroupDiskUsed|最大计算组存储水位超过80%|Failed|Critical|
|Exception|InstanceDown|实例服务不可用|Failed|Critical|
|Exception|LongTransaction|长事务数大于等于5|Failed|Critical|
|Exception|MasterCpuHigh|Master节点CPU水位超过90%|Failed|Critical|
|Exception|MasterMemoryHigh|Master节点内存水位超过85%|Failed|Critical|
|Exception|NonSuperConnection|实例连接数超过80%|Failed|Critical|

