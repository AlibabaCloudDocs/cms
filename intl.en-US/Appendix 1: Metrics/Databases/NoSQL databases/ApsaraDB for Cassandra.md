# ApsaraDB for Cassandra

This topic describes the metrics for ApsaraDB for Cassandra.

-   Set the **Namespace** parameter to **acs\_cds**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|AntiEntropy Active Tasks|Counts|AntiEntropyActiveTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|AntiEntropy Pending Tasks|Counts|AntiEntropyPendingTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Auth Failure|Counts|AuthFailure|userId, clusterId, and host|Average, Maximum, and Minimum|
|CAS Read Latency|ms|CasReadLatency|userId, clusterId, and host|Average, Maximum, and Minimum|
|CAS Read Request|Requests/s|CasReadRequest|userId, clusterId, and host|Average, Maximum, and Minimum|
|CAS Read Unfinished Commit|Counts/s|CasReadUnfinishedCommit|userId, clusterId, and host|Average, Maximum, and Minimum|
|CAS Write Latency|ms|CasWriteLatency|userId, clusterId, and host|Average, Maximum, and Minimum|
|CAS Write Request|Requests/s|CasWriteRequest|userId, clusterId, and host|Average, Maximum, and Minimum|
|CAS Write Unfinished Commit|Counts/s|CasWriteUnfinishedCommit|userId, clusterId, and host|Average, Maximum, and Minimum|
|Client Connection|Connections|ClientConnection|userId, clusterId, and host|Average, Maximum, and Minimum|
|Major GC Elapsed|ms|CmsGc|userId, clusterId, and host|Average, Maximum, and Minimum|
|Commitlog Complete Tasks|Counts|CommitlogCompleteTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Commitlog Pending Tasks|Counts|CommitlogPendingTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Compaction Active Tasks|Counts|CompactionActiveTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Compaction Compacted Bytes|Bytes|CompactionCompactedBytes|userId, clusterId, and host|Average, Maximum, and Minimum|
|Compaction Complete Tasks|Counts|CompactionCompleteTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Compaction Pending Tasks|Counts|CompactionPendingTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Counter Stage Pending Tasks|Counts|CounterStagePendingTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|CPU Hard Interrupt|%|CpuIrq|userId, clusterId, and host|Average, Maximum, and Minimum|
|CPU Load 1m|None|CpuLoad1|userId, clusterId, and host|Average, Maximum, and Minimum|
|CPU Load 15m|None|CpuLoad15|userId, clusterId, and host|Average, Maximum, and Minimum|
|CPU Load 5m|None|CpuLoad5|userId, clusterId, and host|Average, Maximum, and Minimum|
|CPU Nice|%|CpuNice|userId, clusterId, and host|Average, Maximum, and Minimum|
|CPU Soft Interrupt|%|CpuSoftIrq|userId, clusterId, and host|Average, Maximum, and Minimum|
|CPU System|%|CpuSys|userId, clusterId, and host|Average, Maximum, and Minimum|
|CPU Usage|%|CpuUsage|userId, clusterId, and host|Average, Maximum, and Minimum|
|CPU User|%|CpuUser|userId, clusterId, and host|Average, Maximum, and Minimum|
|CPU Wait|%|CpuWait|userId, clusterId, and host|Average, Maximum, and Minimum|
|Data Disk Total|Bytes|DataDiskTotal|userId, clusterId, and host|Average, Maximum, and Minimum|
|Data Disk Usage|%|DataDiskUsage|userId, clusterId, and host|Average, Maximum, and Minimum|
|Data Disk Used|Bytes|DataDiskUsed|userId, clusterId, and host|Average, Maximum, and Minimum|
|Delete With Condition|Requests|DeleteWithCondition|userId, clusterId, and host|Average, Maximum, and Minimum|
|Disk Await|ms|DiskAwait|userId, clusterId, and host|Average, Maximum, and Minimum|
|Data Inputs|Operations/s|DiskInputs|userId, clusterId, and host|Average, Maximum, and Minimum|
|Disk Outputs|Operations/s|DiskOutputs|userId, clusterId, and host|Average, Maximum, and Minimum|
|Disk Reads|Bytes/s|DiskReads|userId, clusterId, and host|Average, Maximum, and Minimum|
|Disk IO %util|%|DiskUtil|userId, clusterId, and host|Average, Maximum, and Minimum|
|Disk Writes|Bytes/s|DiskWrites|userId, clusterId, and host|Average, Maximum, and Minimum|
|Failures|Counts|Failures|userId, clusterId, and host|Average, Maximum, and Minimum|
|Gc Collections|Counts|GcCollections|userId, clusterId, and host|Average, Maximum, and Minimum|
|Gc Max Elapsed|ms|GcMaxElapsed|userId, clusterId, and host|Average, Maximum, and Minimum|
|Gc Reclaimed|Bytes|GcReclaimed|userId, clusterId, and host|Average, Maximum, and Minimum|
|Gc Total Elapsed|ms|GcTotalElapsed|userId, clusterId, and host|Average, Maximum, and Minimum|
|Gossip Active Tasks|Counts|GossipActiveTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Gossip Pending Tasks|Counts|GossipPendingTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Heap Mem Usage|%|HeapMemUsage|userId, clusterId, and host|Average, Maximum, and Minimum|
|Hint Dispatcher Active Tasks|Counts|HintDispatcherActiveTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Hint Dispatcher Pending Tasks|Counts|HintDispatcherPendingTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Key Cache Hit Rate|%|KeyCacheHitRate|userId, clusterId, and host|Average, Maximum, and Minimum|
|Key Cache Hits|Hits/s|KeyCacheHits|userId, clusterId, and host|Average, Maximum, and Minimum|
|Key Cache Requests|Requests/s|KeyCacheRequests|userId, clusterId, and host|Average, Maximum, and Minimum|
|Latency|ms|Latency|userId, clusterId, and host|Average, Maximum, and Minimum|
|Mem Free|Bytes|MemFree|userId, clusterId, and host|Average, Maximum, and Minimum|
|Mem Usage|%|MemUsage|userId, clusterId, and host|Average, Maximum, and Minimum|
|Mem Used|Bytes|MemUsed|userId, clusterId, and host|Average, Maximum, and Minimum|
|Memtable Flush Writer Pending Tasks|Counts|MemtableFlushWriterPendingTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Memtable Post Flush Pending Tasks|Counts|MemtablePostFlushPendingTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Mutation Stage Pending Tasks|Counts|MutationStagePendingTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Native Transport Pending Tasks|Counts|NativeTransportPendingTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Net Input Dropped|Packets/s|NetInputDropped|userId, clusterId, and host|Average, Maximum, and Minimum|
|Net Input Errors|Packets/s|NetInputErrors|userId, clusterId, and host|Average, Maximum, and Minimum|
|Net Input Overruns|Packets/s|NetInputOverruns|userId, clusterId, and host|Average, Maximum, and Minimum|
|Net Inputs|Packets/s|NetInputs|userId, clusterId, and host|Average, Maximum, and Minimum|
|Net Output Dropped|Packets/s|NetOutputDropped|userId, clusterId, and host|Average, Maximum, and Minimum|
|Net Output Errors|Packets/s|NetOutputErrors|userId, clusterId, and host|Average, Maximum, and Minimum|
|Net Output Overruns|Packets/s|NetOutputOverruns|userId, clusterId, and host|Average, Maximum, and Minimum|
|Net Outputs|Packets/s|NetOutputs|userId, clusterId, and host|Average, Maximum, and Minimum|
|Net Reads|Bytes/s|NetReads|userId, clusterId, and host|Average, Maximum, and Minimum|
|Net Writes|Bytes/s|NetWrites|userId, clusterId, and host|Average, Maximum, and Minimum|
|Off Heap Memory|Bytes|OffHeapMem|userId, clusterId, and host|Average, Maximum, and Minimum|
|Minor GC Elapsed|ms|ParNewGc|userId, clusterId, and host|Average, Maximum, and Minimum|
|Parallel Scan|Requests|ParallelScan|userId, clusterId, and host|Average, Maximum, and Minimum|
|Put With Condition|Requests|PutWithCondition|userId, clusterId, and host|Average, Maximum, and Minimum|
|Query With Filter|Requests|QueryWithFilter|userId, clusterId, and host|Average, Maximum, and Minimum|
|Range Slice Latency|ms|RangeSliceLatency|userId, clusterId, and host|Average, Maximum, and Minimum|
|Range Slice Request|Requests/s|RangeSliceRequest|userId, clusterId, and host|Average, Maximum, and Minimum|
|Read Latency|ms|ReadLatency|userId, clusterId, and host|Average, Maximum, and Minimum|
|Read Latency 95th Percentile|ms|ReadLatency95|userId, clusterId, and host|Average, Maximum, and Minimum|
|Read Latency 99th Percentile|ms|ReadLatency99|userId, clusterId, and host|Average, Maximum, and Minimum|
|Read Repair Stage Pending Tasks|Counts|ReadRepairStagePendingTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Read Request|Requests/s|ReadRequest|userId, clusterId, and host|Average, Maximum, and Minimum|
|Read Stage Pending Tasks|Counts|ReadStagePendingTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|Requests|Requests|Request|userId, clusterId, and host|Average, Maximum, and Minimum|
|Row Cache Hit Rate|%|RowCacheHitRate|userId, clusterId, and host|Average, Maximum, and Minimum|
|Row Cache Hits|Hits/s|RowCacheHits|userId, clusterId, and host|Average, Maximum, and Minimum|
|Row Cache Requests|Requests/s|RowCacheRequests|userId, clusterId, and host|Average, Maximum, and Minimum|
|Scan With Filter|Requests|ScanWithFilter|userId, clusterId, and host|Average, Maximum, and Minimum|
|Secondary Index Pending Tasks|Counts|SecondaryIndexPendingTasks|userId, clusterId, and host|Average, Maximum, and Minimum|
|System Disk Usage|%|SysDiskUsage|userId, clusterId, and host|Average, Maximum, and Minimum|
|Timeouts|Counts|Timeouts|userId, clusterId, and host|Average, Maximum, and Minimum|
|Unavailables|Counts|Unavailables|userId, clusterId, and host|Average, Maximum, and Minimum|
|Update With Condition|Requests|UpdateWithCondition|userId, clusterId, and host|Average, Maximum, and Minimum|
|View Write Latency|ms|ViewWriteLatency|userId, clusterId, and host|Average, Maximum, and Minimum|
|View Write Request|Requests/s|ViewWriteRequest|userId, clusterId, and host|Average, Maximum, and Minimum|
|Write Latency|ms|WriteLatency|userId, clusterId, and host|Average, Maximum, and Minimum|
|Write Latency 95th Percentile|ms|WriteLatency95|userId, clusterId, and host|Average, Maximum, and Minimum|
|Write Latency 99th Percentile|ms|WriteLatency99|userId, clusterId, and host|Average, Maximum, and Minimum|
|Write Request|Requests/s|WriteRequest|userId, clusterId, and host|Average, Maximum, and Minimum|

