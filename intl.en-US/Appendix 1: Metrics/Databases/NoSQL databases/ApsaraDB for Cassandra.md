# ApsaraDB for Cassandra

This topic describes the metrics for ApsaraDB for Cassandra.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for ApsaraDB for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_cds**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|AntiEntropy Active Tasks|count|AntiEntropyActiveTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|AntiEntropy Pending Tasks|count|AntiEntropyPendingTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Auth Failure|count|AuthFailure|userId, clusterId, and host|Average, Maximum, and Minimum|
|CAS Read Latency|ms|CasReadLatency|userId, clusterId, and host|Average, Maximum, and Minimum|
|CAS Read Request|count/s|CasReadRequest|userId, clusterId, and host|Average, Maximum, and Minimum|
|CAS Read Unfinished Commit|count/s|CasReadUnfinishedCommit|userId, clusterId, and host|Average, Maximum, and Minimum|
|CAS Write Latency|ms|CasWriteLatency|userId, clusterId, and host|Average, Maximum, and Minimum|
|CAS Write Request|count/s|CasWriteRequest|userId, clusterId, and host|Average, Maximum, and Minimum|
|CAS Write Unfinished Commit|count/s|CasWriteUnfinishedCommit|userId, clusterId, and host|Average, Maximum, and Minimum|
|Client Connection|count|ClientConnection|userId, clusterId, and host|Average, Maximum, and Minimum|
|Major GC Elapsed|ms|CmsGc|userId, clusterId, and host|Average, Maximum, and Minimum|
|Commitlog Complete Tasks|count|CommitlogCompleteTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Commitlog Pending Tasks|count|CommitlogPendingTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Compaction Active Tasks|count|CompactionActiveTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Compaction Compacted Bytes|byte|CompactionCompactedBytes|userId, clusterId, and host|Average, Maximum, and Minimum|
|Compaction Complete Tasks|count|CompactionCompleteTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Compaction Pending Tasks|count|CompactionPendingTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Counter Stage Pending Tasks|count|CounterStagePendingTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|CPU Hard Interrupt|%|CpuIrq|userId, clusterId, and host|Average, Maximum, and Minimum|
|CPU Load 1m|N/A|CpuLoad1|userId, clusterId, and host|Average, Maximum, and Minimum|
|CPU Load 15m|N/A|CpuLoad15|userId, clusterId, and host|Average, Maximum, and Minimum|
|CPU Load 5m|N/A|CpuLoad5|userId, clusterId, and host|Average, Maximum, and Minimum|
|CPU Nice|%|CpuNice|userId, clusterId, and host|Average, Maximum, and Minimum|
|CPU Soft Interrupt|%|CpuSoftIrq|userId, clusterId, and host|Average, Maximum, and Minimum|
|CPU System|%|CpuSys|userId, clusterId, and host|Average, Maximum, and Minimum|
|CPU Usage|%|CpuUsage|userId, clusterId, and host|Average, Maximum, and Minimum|
|CPU User|%|CpuUser|userId, clusterId, and host|Average, Maximum, and Minimum|
|CPU Wait|%|CpuWait|userId, clusterId, and host|Average, Maximum, and Minimum|
|Data Disk Total|byte|DataDiskTotal|userId, clusterId, and host|Average, Maximum, and Minimum|
|Data Disk Usage|%|DataDiskUsage|userId, clusterId, and host|Average, Maximum, and Minimum|
|Data Disk Used|byte|DataDiskUsed|userId, clusterId, and host|Average, Maximum, and Minimum|
|Delete With Condition|count|DeleteWithCondition|userId, clusterId, and host|Average, Maximum, and Minimum|
|Disk Await|ms|DiskAwait|userId, clusterId, and host|Average, Maximum, and Minimum|
|Data Inputs|count/s|DiskInputs|userId, clusterId, and host|Average, Maximum, and Minimum|
|Disk Outputs|count/s|DiskOutputs|userId, clusterId, and host|Average, Maximum, and Minimum|
|Disk Reads|byte/s|DiskReads|userId, clusterId, and host|Average, Maximum, and Minimum|
|Disk IO %util|%|DiskUtil|userId, clusterId, and host|Average, Maximum, and Minimum|
|Disk Writes|byte/s|DiskWrites|userId, clusterId, and host|Average, Maximum, and Minimum|
|Failures|count|Failures|userId, clusterId, and host|Average, Maximum, and Minimum|
|Gc Collections|count|GcCollections|userId, clusterId, and host|Average, Maximum, and Minimum|
|Gc Max Elapsed|ms|GcMaxElapsed|userId, clusterId, and host|Average, Maximum, and Minimum|
|Gc Reclaimed|byte|GcReclaimed|userId, clusterId, and host|Average, Maximum, and Minimum|
|Gc Total Elapsed|ms|GcTotalElapsed|userId, clusterId, and host|Average, Maximum, and Minimum|
|Gossip Active Tasks|count|GossipActiveTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Gossip Pending Tasks|count|GossipPendingTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Heap Mem Usage|%|HeapMemUsage|userId, clusterId, and host|Average, Maximum, and Minimum|
|Hint Dispatcher Active Tasks|count|HintDispatcherActiveTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Hint Dispatcher Pending Tasks|count|HintDispatcherPendingTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Key Cache Hit Rate|%|KeyCacheHitRate|userId, clusterId, and host|Average, Maximum, and Minimum|
|Key Cache Hits|count/s|KeyCacheHits|userId, clusterId, and host|Average, Maximum, and Minimum|
|Key Cache Requests|count/s|KeyCacheRequests|userId, clusterId, and host|Average, Maximum, and Minimum|
|Latency|ms|Latency|userId, clusterId, and host|Average, Maximum, and Minimum|
|Mem Free|byte|MemFree|userId, clusterId, and host|Average, Maximum, and Minimum|
|Mem Usage|%|MemUsage|userId, clusterId, and host|Average, Maximum, and Minimum|
|Mem Used|byte|MemUsed|userId, clusterId, and host|Average, Maximum, and Minimum|
|Memtable Flush Writer Pending Tasks|count|MemtableFlushWriterPendingTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Memtable Post Flush Pending Tasks|count|MemtablePostFlushPendingTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Mutation Stage Pending Tasks|count|MutationStagePendingTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Native Transport Pending Tasks|count|NativeTransportPendingTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Net Input Dropped|packet/s|NetInputDropped|userId, clusterId, and host|Average, Maximum, and Minimum|
|Net Input Errors|packet/s|NetInputErrors|userId, clusterId, and host|Average, Maximum, and Minimum|
|Net Input Overruns|packet/s|NetInputOverruns|userId, clusterId, and host|Average, Maximum, and Minimum|
|Net Inputs|packet/s|NetInputs|userId, clusterId, and host|Average, Maximum, and Minimum|
|Net Output Dropped|packet/s|NetOutputDropped|userId, clusterId, and host|Average, Maximum, and Minimum|
|Net Output Errors|packet/s|NetOutputErrors|userId, clusterId, and host|Average, Maximum, and Minimum|
|Net Output Overruns|packet/s|NetOutputOverruns|userId, clusterId, and host|Average, Maximum, and Minimum|
|Net Outputs|packet/s|NetOutputs|userId, clusterId, and host|Average, Maximum, and Minimum|
|Net Reads|byte/s|NetReads|userId, clusterId, and host|Average, Maximum, and Minimum|
|Net Writes|byte/s|NetWrites|userId, clusterId, and host|Average, Maximum, and Minimum|
|Off Heap Memory|byte|OffHeapMem|userId, clusterId, and host|Average, Maximum, and Minimum|
|Minor GC Elapsed|ms|ParNewGc|userId, clusterId, and host|Average, Maximum, and Minimum|
|Parallel Scan|count|ParallelScan|userId, clusterId, and host|Average, Maximum, and Minimum|
|Put With Condition|count|PutWithCondition|userId, clusterId, and host|Average, Maximum, and Minimum|
|Query With Filter|count|QueryWithFilter|userId, clusterId, and host|Average, Maximum, and Minimum|
|Range Slice Latency|ms|RangeSliceLatency|userId, clusterId, and host|Average, Maximum, and Minimum|
|Range Slice Request|count/s|RangeSliceRequest|userId, clusterId, and host|Average, Maximum, and Minimum|
|Read Latency|ms|ReadLatency|userId, clusterId, and host|Average, Maximum, and Minimum|
|Read Latency 95th Percentile|ms|ReadLatency95|userId, clusterId, and host|Average, Maximum, and Minimum|
|Read Latency 99th Percentile|ms|ReadLatency99|userId, clusterId, and host|Average, Maximum, and Minimum|
|Read Repair Stage Pending Tasks|count|ReadRepairStagePendingTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Read Request|count/s|ReadRequest|userId, clusterId, and host|Average, Maximum, and Minimum|
|Read Stage Pending Tasks|count|ReadStagePendingTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Requests|count|Request|userId, clusterId, and host|Average, Maximum, and Minimum|
|Row Cache Hit Rate|%|RowCacheHitRate|userId, clusterId, and host|Average, Maximum, and Minimum|
|Row Cache Hits|count/s|RowCacheHits|userId, clusterId, and host|Average, Maximum, and Minimum|
|Row Cache Requests|count/s|RowCacheRequests|userId, clusterId, and host|Average, Maximum, and Minimum|
|Scan With Filter|count|ScanWithFilter|userId, clusterId, and host|Average, Maximum, and Minimum|
|Secondary Index Pending Tasks|count|SecondaryIndexPendingTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|System Disk Usage|%|SysDiskUsage|userId, clusterId, and host|Average, Maximum, and Minimum|
|Timeouts|count|Timeouts|userId, clusterId, and host|Average, Maximum, and Minimum|
|Unavailables|count|Unavailables|userId, clusterId, and host|Average, Maximum, and Minimum|
|Update With Condition|count|UpdateWithCondition|userId, clusterId, and host|Average, Maximum, and Minimum|
|View Write Latency|ms|ViewWriteLatency|userId, clusterId, and host|Average, Maximum, and Minimum|
|View Write Request|count/s|ViewWriteRequest|userId, clusterId, and host|Average, Maximum, and Minimum|
|Write Latency|ms|WriteLatency|userId, clusterId, and host|Average, Maximum, and Minimum|
|Write Latency 95th Percentile|ms|WriteLatency95|userId, clusterId, and host|Average, Maximum, and Minimum|
|Write Latency 99th Percentile|ms|WriteLatency99|userId, clusterId, and host|Average, Maximum, and Minimum|
|Write Request|count/s|WriteRequest|userId, clusterId, and host|Average, Maximum, and Minimum|

