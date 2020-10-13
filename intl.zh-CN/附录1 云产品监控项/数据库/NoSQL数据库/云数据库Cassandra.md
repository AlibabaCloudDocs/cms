# 云数据库Cassandra

通过本文您可以了解云数据库Cassandra的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_cds**。
-   **Period**默认为60秒，也可以为60的整数倍。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|AntiEntropy活跃任务数|Counts|AntiEntropyActiveTasks|userId、clusterId、host|Average、Maximum、Minimum|
|AntiEntropy等待任务数|Counts|AntiEntropyPendingTasks|userId、clusterId、host|Average、Maximum、Minimum|
|认证失败次数|Counts|AuthFailure|userId、clusterId、host|Average、Maximum、Minimum|
|CAS读延时|ms|CasReadLatency|userId、clusterId、host|Average、Maximum、Minimum|
|CAS读请求次数|Requests/s|CasReadRequest|userId、clusterId、host|Average、Maximum、Minimum|
|CAS读请求未提交次数|Counts/s|CasReadUnfinishedCommit|userId、clusterId、host|Average、Maximum、Minimum|
|CAS写延时|ms|CasWriteLatency|userId、clusterId、host|Average、Maximum、Minimum|
|CAS写请求次数|Requests/s|CasWriteRequest|userId、clusterId、host|Average、Maximum、Minimum|
|CAS写请求未提交次数|Counts/s|CasWriteUnfinishedCommit|userId、clusterId、host|Average、Maximum、Minimum|
|客户端连接数|Connections|ClientConnection|userId、clusterId、host|Average、Maximum、Minimum|
|Major GC耗时|ms|CmsGc|userId、clusterId、host|Average、Maximum、Minimum|
|Commitlog完成任务数|Counts|CommitlogCompleteTasks|userId、clusterId、host|Average、Maximum、Minimum|
|Commitlog等待任务数|Counts|CommitlogPendingTasks|userId、clusterId、host|Average、Maximum、Minimum|
|Compaction活跃任务数|Counts|CompactionActiveTasks|userId、clusterId、host|Average、Maximum、Minimum|
|Compaction已完成数据|Bytes|CompactionCompactedBytes|userId、clusterId、host|Average、Maximum、Minimum|
|Compaction完成任务数|Counts|CompactionCompleteTasks|userId、clusterId、host|Average、Maximum、Minimum|
|Compaction等待任务数|Counts|CompactionPendingTasks|userId、clusterId、host|Average、Maximum、Minimum|
|CounterStage等待任务数|Counts|CounterStagePendingTasks|userId、clusterId、host|Average、Maximum、Minimum|
|CPU硬中断|%|CpuIrq|userId、clusterId、host|Average、Maximum、Minimum|
|CPU 1分钟负载|无|CpuLoad1|userId、clusterId、host|Average、Maximum、Minimum|
|CPU 15分钟负载|无|CpuLoad15|userId、clusterId、host|Average、Maximum、Minimum|
|CPU 5分钟负载|无|CpuLoad5|userId、clusterId、host|Average、Maximum、Minimum|
|CPU Nice占比|%|CpuNice|userId、clusterId、host|Average、Maximum、Minimum|
|CPU软中断|%|CpuSoftIrq|userId、clusterId、host|Average、Maximum、Minimum|
|CPU系统占比|%|CpuSys|userId、clusterId、host|Average、Maximum、Minimum|
|CPU使用率|%|CpuUsage|userId、clusterId、host|Average、Maximum、Minimum|
|CPU用户占比|%|CpuUser|userId、clusterId、host|Average、Maximum、Minimum|
|CPU等待|%|CpuWait|userId、clusterId、host|Average、Maximum、Minimum|
|数据盘大小|Bytes|DataDiskTotal|userId、clusterId、host|Average、Maximum、Minimum|
|数据盘使用率|%|DataDiskUsage|userId、clusterId、host|Average、Maximum、Minimum|
|数据盘使用|Bytes|DataDiskUsed|userId、clusterId、host|Average、Maximum、Minimum|
|DeleteWithCondition请求数|Requests|DeleteWithCondition|userId、clusterId、host|Average、Maximum、Minimum|
|磁盘等待|ms|DiskAwait|userId、clusterId、host|Average、Maximum、Minimum|
|磁盘读次数|Operations/s|DiskInputs|userId、clusterId、host|Average、Maximum、Minimum|
|磁盘写次数|Operations/s|DiskOutputs|userId、clusterId、host|Average、Maximum、Minimum|
|磁盘读数据|Bytes/s|DiskReads|userId、clusterId、host|Average、Maximum、Minimum|
|磁盘%util|%|DiskUtil|userId、clusterId、host|Average、Maximum、Minimum|
|磁盘写数据|Bytes/s|DiskWrites|userId、clusterId、host|Average、Maximum、Minimum|
|请求失败数|Counts|Failures|userId、clusterId、host|Average、Maximum、Minimum|
|GC次数|Counts|GcCollections|userId、clusterId、host|Average、Maximum、Minimum|
|GC最大耗时|ms|GcMaxElapsed|userId、clusterId、host|Average、Maximum、Minimum|
|GC回收内存|Bytes|GcReclaimed|userId、clusterId、host|Average、Maximum、Minimum|
|GC总耗时|ms|GcTotalElapsed|userId、clusterId、host|Average、Maximum、Minimum|
|Gossip活跃任务数|Counts|GossipActiveTasks|userId、clusterId、host|Average、Maximum、Minimum|
|Gossip等待任务数|Counts|GossipPendingTasks|userId、clusterId、host|Average、Maximum、Minimum|
|堆内存使用率|%|HeapMemUsage|userId、clusterId、host|Average、Maximum、Minimum|
|HintDispatcher活跃任务数|Counts|HintDispatcherActiveTasks|userId、clusterId、host|Average、Maximum、Minimum|
|HintDispatcher等待任务数|Counts|HintDispatcherPendingTasks|userId、clusterId、host|Average、Maximum、Minimum|
|Key Cache命中率|%|KeyCacheHitRate|userId、clusterId、host|Average、Maximum、Minimum|
|Key Cache命中次数|Hits/s|KeyCacheHits|userId、clusterId、host|Average、Maximum、Minimum|
|Key Cache请求次数|Requests/s|KeyCacheRequests|userId、clusterId、host|Average、Maximum、Minimum|
|延时|ms|Latency|userId、clusterId、host|Average、Maximum、Minimum|
|内存剩余|Bytes|MemFree|userId、clusterId、host|Average、Maximum、Minimum|
|内存使用率|%|MemUsage|userId、clusterId、host|Average、Maximum、Minimum|
|内存使用|Bytes|MemUsed|userId、clusterId、host|Average、Maximum、Minimum|
|MemtableFlushWriter活跃任务数|Counts|MemtableFlushWriterPendingTasks|userId、clusterId、host|Average、Maximum、Minimum|
|MemtablePostFlush等待任务数|Counts|MemtablePostFlushPendingTasks|userId、clusterId、host|Average、Maximum、Minimum|
|MutationStage等待任务数|Counts|MutationStagePendingTasks|userId、clusterId、host|Average、Maximum、Minimum|
|NativeTransport等待任务数|Counts|NativeTransportPendingTasks|userId、clusterId、host|Average、Maximum、Minimum|
|网络收包丢失数|Packets/s|NetInputDropped|userId、clusterId、host|Average、Maximum、Minimum|
|网络收包错误数|Packets/s|NetInputErrors|userId、clusterId、host|Average、Maximum、Minimum|
|网络收包Overruns|Packets/s|NetInputOverruns|userId、clusterId、host|Average、Maximum、Minimum|
|网络收包数|Packets/s|NetInputs|userId、clusterId、host|Average、Maximum、Minimum|
|网络发包丢失数|Packets/s|NetOutputDropped|userId、clusterId、host|Average、Maximum、Minimum|
|网络发包错误数|Packets/s|NetOutputErrors|userId、clusterId、host|Average、Maximum、Minimum|
|网络发包Overruns|Packets/s|NetOutputOverruns|userId、clusterId、host|Average、Maximum、Minimum|
|网络发包数|Packets/s|NetOutputs|userId、clusterId、host|Average、Maximum、Minimum|
|网络收数据|Bytes/s|NetReads|userId、clusterId、host|Average、Maximum、Minimum|
|网络发数据|Bytes/s|NetWrites|userId、clusterId、host|Average、Maximum、Minimum|
|非堆内存|Bytes|OffHeapMem|userId、clusterId、host|Average、Maximum、Minimum|
|Minor GC耗时|ms|ParNewGc|userId、clusterId、host|Average、Maximum、Minimum|
|ParallelScan请求数|Requests|ParallelScan|userId、clusterId、host|Average、Maximum、Minimum|
|PutWithCondition请求数|Requests|PutWithCondition|userId、clusterId、host|Average、Maximum、Minimum|
|QueryWithFilter请求数|Requests|QueryWithFilter|userId、clusterId、host|Average、Maximum、Minimum|
|Range切片延时|ms|RangeSliceLatency|userId、clusterId、host|Average、Maximum、Minimum|
|Range切片请求次数|Requests/s|RangeSliceRequest|userId、clusterId、host|Average、Maximum、Minimum|
|读延时|ms|ReadLatency|userId、clusterId、host|Average、Maximum、Minimum|
|读延时95分位|ms|ReadLatency95|userId、clusterId、host|Average、Maximum、Minimum|
|读延时99分位|ms|ReadLatency99|userId、clusterId、host|Average、Maximum、Minimum|
|ReadRepairStage等待任务数|Counts|ReadRepairStagePendingTasks|userId、clusterId、host|Average、Maximum、Minimum|
|读请求次数|Requests/s|ReadRequest|userId、clusterId、host|Average、Maximum、Minimum|
|ReadStage等待任务数|Counts|ReadStagePendingTasks|userId、clusterId、host|Average、Maximum、Minimum|
|请求数|Requests|Request|userId、clusterId、host|Average、Maximum、Minimum|
|Row Cache命中率|%|RowCacheHitRate|userId、clusterId、host|Average、Maximum、Minimum|
|Row Cache命中次数|Hits/s|RowCacheHits|userId、clusterId、host|Average、Maximum、Minimum|
|Row Cache请求次数|Requests/s|RowCacheRequests|userId、clusterId、host|Average、Maximum、Minimum|
|ScanWithFilter请求数|Requests|ScanWithFilter|userId、clusterId、host|Average、Maximum、Minimum|
|二级索引等待任务数|Counts|SecondaryIndexPendingTasks|userId、clusterId、host|Average、Maximum、Minimum|
|系统盘使用率|%|SysDiskUsage|userId、clusterId、host|Average、Maximum、Minimum|
|超时次数|Counts|Timeouts|userId、clusterId、host|Average、Maximum、Minimum|
|请求不可用数|Counts|Unavailables|userId、clusterId、host|Average、Maximum、Minimum|
|UpdateWithCondition请求数|Requests|UpdateWithCondition|userId、clusterId、host|Average、Maximum、Minimum|
|视图写延时|ms|ViewWriteLatency|userId、clusterId、host|Average、Maximum、Minimum|
|视图写请求次数|Requests/s|ViewWriteRequest|userId、clusterId、host|Average、Maximum、Minimum|
|写延时|ms|WriteLatency|userId、clusterId、host|Average、Maximum、Minimum|
|写延时95分位|ms|WriteLatency95|userId、clusterId、host|Average、Maximum、Minimum|
|写延时99分位|ms|WriteLatency99|userId、clusterId、host|Average、Maximum、Minimum|
|写请求次数|Requests/s|WriteRequest|userId、clusterId、host|Average、Maximum、Minimum|

