# HBase

This topic describes the metrics for ApsaraDB for HBase Standard Edition.

-   Set the **Namespace** parameter to **acs\_hbase**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|ActiveApplications|N/A|ActiveApplications|userId, clusterId, and role|Average|
|AggregatecontainersAllocated|N/A|AggregatecontainersAllocated|userId, clusterId, and role|Average|
|AggregatecontainersReleased|N/A|AggregatecontainersReleased|userId, clusterId, and role|Average|
|AliveHandlerNum|N/A|AliveHandlerNum|userId, clusterId, and role|Average|
|Append\_Mean|N/A|Append\_Mean|userId, clusterId, and role|Average|
|Append\_num\_ops|N/A|Append\_num\_ops|userId, clusterId, and role|Average|
|AppsCompleted|N/A|AppsCompleted|userId, clusterId, and role|Average|
|AppsFailed|N/A|AppsFailed|userId, clusterId, and role|Average|
|AppsKilled|N/A|AppsKilled|userId, clusterId, and role|Average|
|AppsPending|N/A|AppsPending|userId, clusterId, and role|Average|
|AvailableMB|MB|AvailableMB|userId, clusterId, and role|Average|
|AvailableVCores|N/A|AvailableVCores|userId, clusterId, and role|Average|
|BlockCacheCount|N/A|BlockCacheCount|userId, clusterId, and role|Average|
|RegionServer Block Cache Count Hit Percent|N/A|BlockCacheCountHitPercent|userId, clusterId, and role|Average|
|BlockCacheEvictedCount|N/A|BlockCacheEvictedCount|userId, clusterId, and role|Average|
|BlockCacheExpressHitPercent|N/A|BlockCacheExpressHitPercent|userId, clusterId, and role|Average|
|BlockCacheFree|N/A|BlockCacheFree|userId, clusterId, and role|Average|
|BlockCacheHitCount|N/A|BlockCacheHitCount|userId, clusterId, and role|Average|
|BlockCacheMissCount|N/A|BlockCacheMissCount|userId, clusterId, and role|Average|
|BlockCacheSize|N/A|BlockCacheSize|userId, clusterId, and role|Average|
|BlockCapacity|N/A|BlockCapacity|userId, clusterId, and role|Average|
|BlockChecksumOpAvgTime|N/A|BlockChecksumOpAvgTime|userId, clusterId, and role|Average|
|BlockChecksumOpNumOps|N/A|BlockChecksumOpNumOps|userId, clusterId, and role|Average|
|BlockReportsAvgTime|N/A|BlockReportsAvgTime|userId, clusterId, and role|Average|
|BlockReportsNumOps|N/A|BlockReportsNumOps|userId, clusterId, and role|Average|
|BlockVerificationFailures|N/A|BlockVerificationFailures|userId, clusterId, and role|Average|
|BlocksRead|N/A|BlocksRead|userId, clusterId, and role|Average|
|BlocksRemoved|N/A|BlocksRemoved|userId, clusterId, and role|Average|
|BlocksReplicated|N/A|BlocksReplicated|userId, clusterId, and role|Average|
|BlocksTotal|N/A|BlocksTotal|userId, clusterId, and role|Average|
|BlocksUncached|N/A|BlocksUncached|userId, clusterId, and role|Average|
|BlocksVerified|N/A|BlocksVerified|userId, clusterId, and role|Average|
|BlocksWritten|N/A|BlocksWritten|userId, clusterId, and role|Average|
|BytesRead|N/A|BytesRead|userId, clusterId, and role|Average|
|BytesWritten|N/A|BytesWritten|userId, clusterId, and role|Average|
|CallQueueLength|N/A|CallQueueLength|userId, clusterId, and role|Average|
|CapacityRemaining|N/A|CapacityRemaining|userId, clusterId, and role|Average|
|Capacity Total|N/A|CapacityTotal|userId, clusterId, and role|Average|
|Capacity Used|N/A|CapacityUsed|userId, clusterId, and role|Average|
|CapacityUsedNonDFS|N/A|CapacityUsedNonDFS|userId, clusterId, and role|Average|
|Capacity Used Percent|Decimal number between 0 and 1|CapacityUsedPercent|userId, clusterId, and role|Average|
|ClusterRequests|N/A|ClusterRequests|userId, clusterId, and role|Average|
|ContainersIniting|N/A|ContainersIniting|userId, clusterId, and role|Average|
|CopyBlockOpAvgTime|N/A|CopyBlockOpAvgTime|userId, clusterId, and role|Average|
|CopyBlockOpNumOps|N/A|CopyBlockOpNumOps|userId, clusterId, and role|Average|
|CorruptBlocks|N/A|CorruptBlocks|userId, clusterId, and role|Average|
|DeleteRequestLatency\_mean|N/A|DeleteRequestLatency\_mean|userId, clusterId, and role|Average|
|DeleteRequestLatency\_num\_ops|N/A|DeleteRequestLatency\_num\_ops|userId, clusterId, and role|Average|
|ExcessBlocks|N/A|ExcessBlocks|userId, clusterId, and role|Average|
|ExpiredHeartbeats|N/A|ExpiredHeartbeats|userId, clusterId, and role|Average|
|FailedSanityCheckEXception|N/A|FailedSanityCheckEXception|userId, clusterId, and role|Average|
|FlushNanosAvgTime|N/A|FlushNanosAvgTime|userId, clusterId, and role|Average|
|FlushNanosNumOps|N/A|FlushNanosNumOps|userId, clusterId, and role|Average|
|FlushQueueSize|N/A|FlushQueueSize|userId, clusterId, and role|Average|
|FlushTime|N/A|FlushTime|userId, clusterId, and role|Average|
|FlushTime\_num\_ops|N/A|FlushTime\_num\_ops|userId, clusterId, and role|Average|
|FlushedCellsSize|N/A|FlushedCellsSize|userId, clusterId, and role|Average|
|FsPreadLatency\_avg\_time|N/A|FsPreadLatency\_avg\_time|userId, clusterId, and role|Average|
|FsPreadLatency\_num\_ops|N/A|FsPreadLatency\_num\_ops|userId, clusterId, and role|Average|
|FsyncCount|N/A|FsyncCount|userId, clusterId, and role|Average|
|GcCount|N/A|GcCount|userId, clusterId, and role|Average|
|GcTimeMillis|N/A|GcTimeMillis|userId, clusterId, and role|Average|
|RegionServer Get Request Latency|N/A|GetRequestLatency\_mean|userId, clusterId, and role|Average|
|GetRequestLatency\_num\_ops|N/A|GetRequestLatency\_num\_ops|userId, clusterId, and role|Average|
|HOFSAbortUploadException|N/A|HOFSAbortUploadException|userId, clusterId, and role|Average|
|HOFSConfigException|N/A|HOFSConfigException|userId, clusterId, and role|Average|
|HOFSTooManyFileReader|N/A|HOFSTooManyFileReader|userId, clusterId, and role|Average|
|handlerQueueSize|N/A|handlerQueueSize|userId, clusterId, and role|Average|
|HlogCount|N/A|HlogCount|userId, clusterId, and role|Average|
|HlogFileSize|N/A|HlogFileSize|userId, clusterId, and role|Average|
|HlogWriteLatency\_avg\_time|N/A|HlogWriteLatency\_avg\_time|userId, clusterId, and role|Average|
|HlogWriteLatency\_num\_ops|N/A|HlogWriteLatency\_num\_ops|userId, clusterId, and role|Average|
|HlogWriteSize\_avg\_time|N/A|HlogWriteSize\_avg\_time|userId, clusterId, and role|Average|
|HlogWriteSize\_num\_ops|N/A|HlogWriteSize\_num\_ops|userId, clusterId, and role|Average|
|LoadPerCpu|N/A|LoadPerCpu|userId, clusterId, and role|Average|
|MaxRegionSize|N/A|MaxRegionSize|userId, clusterId, and role|Average|
|MemFreePercent|%|MemFreePercent|userId, clusterId, and role|Average|
|MemHeapCommittedM|N/A|MemHeapCommittedM|userId, clusterId, and role|Average|
|MemHeapMaxM|N/A|MemHeapMaxM|userId, clusterId, and role|Average|
|MemHeapUsedM|N/A|MemHeapUsedM|userId, clusterId, and role|Average|
|MemMaxM|N/A|MemMaxM|userId, clusterId, and role|Average|
|MemNonHeapCommittedM|N/A|MemNonHeapCommittedM|userId, clusterId, and role|Average|
|MemNonHeapMaxM|N/A|MemNonHeapMaxM|userId, clusterId, and role|Average|
|MemNonHeapUsedM|N/A|MemNonHeapUsedM|userId, clusterId, and role|Average|
|RegionServer Mem Store Size|N/A|MemStoreSize|userId, clusterId, and role|Average|
|MissingBlocks|N/A|MissingBlocks|userId, clusterId, and role|Average|
|MutationsWithoutWALCount|N/A|MutationsWithoutWALCount|userId, clusterId, and role|Average|
|MutationsWithoutWALSize|N/A|MutationsWithoutWALSize|userId, clusterId, and role|Average|
|NotServeringRegionEXception|N/A|NotServeringRegionEXception|userId, clusterId, and role|Average|
|NumDeadRegionServers|N/A|NumDeadRegionServers|userId, clusterId, and role|Average|
|NumOpenConnections|N/A|NumOpenConnections|userId, clusterId, and role|Average|
|Num Region Servers|N/A|NumRegionServers|userId, clusterId, and role|Average|
|OutOfOrderScannerNextException|N/A|OutOfOrderScannerNextException|userId, clusterId, and role|Average|
|PendingDataNodeMessageCount|N/A|PendingDataNodeMessageCount|userId, clusterId, and role|Average|
|PendingDeletionBlocks|N/A|PendingDeletionBlocks|userId, clusterId, and role|Average|
|PendingReplicationBlocks|N/A|PendingReplicationBlocks|userId, clusterId, and role|Average|
|PercentFilesLocalSecondaryRegions|N/A|PercentFilesLocalSecondaryRegions|userId, clusterId, and role|Average|
|PostponedMisreplicatedBlocks|N/A|PostponedMisreplicatedBlocks|userId, clusterId, and role|Average|
|ReadBlockOpAvgTime|N/A|ReadBlockOpAvgTime|userId, clusterId, and role|Average|
|ReadBlockOpNumOps|N/A|ReadBlockOpNumOps|userId, clusterId, and role|Average|
|ReadRequests\_avg\_time|N/A|ReadRequests\_avg\_time|userId, clusterId, and role|Average|
|RegionServer Read Request Quantity|N/A|ReadRequests\_num\_ops|userId, clusterId, and role|Average|
|ReceivedBytes|N/A|ReceivedBytes|userId, clusterId, and role|Average|
|RegionMovedException|N/A|RegionMovedException|userId, clusterId, and role|Average|
|RegionServerStartTime|N/A|RegionServerStartTime|userId, clusterId, and role|Average|
|RegionServer\_NumOpenConnections|N/A|RegionServer\_NumOpenConnections|userId, clusterId, and role|Average|
|RegionSplitTime\_avg\_time|N/A|RegionSplitTime\_avg\_time|userId, clusterId, and role|Average|
|RegionSplitTime\_num\_ops|N/A|RegionSplitTime\_num\_ops|userId, clusterId, and role|Average|
|RegionTooBusyException|N/A|RegionTooBusyException|userId, clusterId, and role|Average|
|Region Count|N/A|Regions|userId, clusterId, and role|Average|
|ReplaceBlockOpAvgTime|N/A|ReplaceBlockOpAvgTime|userId, clusterId, and role|Average|
|ReplaceBlockOpNumOps|N/A|ReplaceBlockOpNumOps|userId, clusterId, and role|Average|
|Replay\_mean|N/A|Replay\_mean|userId, clusterId, and role|Average|
|Replay\_num\_ops|N/A|Replay\_num\_ops|userId, clusterId, and role|Average|
|ReservedContainers|N/A|ReservedContainers|userId, clusterId, and role|Average|
|ScheduledReplicationBlocks|N/A|ScheduledReplicationBlocks|userId, clusterId, and role|Average|
|SentBytes|N/A|SentBytes|userId, clusterId, and role|Average|
|SlowAppendCount|N/A|SlowAppendCount|userId, clusterId, and role|Average|
|SlowDeleteCount|N/A|SlowDeleteCount|userId, clusterId, and role|Average|
|SlowGetCount|N/A|SlowGetCount|userId, clusterId, and role|Average|
|SlowIncrementCount|N/A|SlowIncrementCount|userId, clusterId, and role|Average|
|SlowPutCount|N/A|SlowPutCount|userId, clusterId, and role|Average|
|SplitQueueLength|N/A|SplitQueueLength|userId, clusterId, and role|Average|
|SplitRequestCount|N/A|SplitRequestCount|userId, clusterId, and role|Average|
|SplitSuccessCount|N/A|SplitSuccessCount|userId, clusterId, and role|Average|
|StaticBloomSize|N/A|StaticBloomSize|userId, clusterId, and role|Average|
|StaticIndexSize|N/A|StaticIndexSize|userId, clusterId, and role|Average|
|StoreFileMeanCount|N/A|StoreFileMeanCount|userId, clusterId, and role|Average|
|StoreFileSize|N/A|StoreFileSize|userId, clusterId, and role|Average|
|StoreFiles|N/A|StoreFiles|userId, clusterId, and role|Average|
|StorefileIndexSize|N/A|StorefileIndexSize|userId, clusterId, and role|Average|
|StorefileUncompressedSize|N/A|StorefileUncompressedSize|userId, clusterId, and role|Average|
|Stores|N/A|Stores|userId, clusterId, and role|Average|
|StreamingInputRate|%|StreamingInputRate|userId, clusterId, and appId|Average|
|StreamingLatency|%|StreamingLatency|userId, clusterId, and appId|Average|
|ThreadsBlocked|N/A|ThreadsBlocked|userId, clusterId, and role|Average|
|ThreadsNew|N/A|ThreadsNew|userId, clusterId, and role|Average|
|ThreadsRunnable|N/A|ThreadsRunnable|userId, clusterId, and role|Average|
|ThreadsTerminated|N/A|ThreadsTerminated|userId, clusterId, and role|Average|
|ThreadsTimedWaiting|N/A|ThreadsTimedWaiting|userId, clusterId, and role|Average|
|ThreadsWaiting|N/A|ThreadsWaiting|userId, clusterId, and role|Average|
|TotalFiles|N/A|TotalFiles|userId, clusterId, and role|Average|
|TotalLoad|N/A|TotalLoad|userId, clusterId, and role|Average|
|Total Number of Requests|N/A|TotalRequestCount|userId, clusterId, and role|Average|
|UnderReplicatedBlocks|N/A|UnderReplicatedBlocks|userId, clusterId, and role|Average|
|UnknowScannerException|N/A|UnknowScannerException|userId, clusterId, and role|Average|
|VolumeFailures|N/A|VolumeFailures|userId, clusterId, and role|Average|
|WriteBlockOpAvgTime|N/A|WriteBlockOpAvgTime|userId, clusterId, and role|Average|
|WriteBlockOpNumops|N/A|WriteBlockOpNumops|userId, clusterId, and role|Average|
|WriteRequests\_avg\_time|N/A|WriteRequests\_avg\_time|userId, clusterId, and role|Average|
|RegionServer Write Request Quantity|N/A|WriteRequests\_num\_ops|userId, clusterId, and role|Average|
|Network inflow per second|N/A|bytes\_in|userId, clusterId, and role|Average|
|Network outflow per second|N/A|bytes\_out|userId, clusterId, and role|Average|
|RegionServer Compaction Queue Size|N/A|compactionQueueSize|userId, clusterId, and role|Average|
|CPU idle|N/A|cpu\_idle|userId, clusterId, and role|Average|
|System state CPU Usage|N/A|cpu\_system|userId, clusterId, and role|Average|
|User CPU Usage|N/A|cpu\_user|userId, clusterId, and role|Average|
|Free Disk Size|N/A|disk\_total|userId, clusterId, and role|Average|
|System Disk Remaining Space|N/A|disk\_free\_percent\_rootfs|userId, clusterId, and role|Average|
|Total Disk Size|N/A|disk\_total|userId, clusterId, and role|Average|
|Average Load in 15 minutes|N/A|load\_fifteen|userId, clusterId, and role|Average|
|Average Load in 5 minute|N/A|load\_five|userId, clusterId, and role|Average|
|Average Load in 1 minute|N/A|load\_one|userId, clusterId, and role|Average|
|Free Memory Size|N/A|mem\_free|userId, clusterId, and role|Average|
|Total Memory Size|N/A|mem\_total|userId, clusterId, and role|Average|
|NumCallsInPriorityQueue|N/A|numCallsInPriorityQueue|userId, clusterId, and role|Average|
|NumCallsInReplicationQueue|N/A|NumCallsInReplicationQueue|userId, clusterId, and role|Average|
|Inbound Data Package Rate|N/A|pkts\_in|userId, clusterId, and role|Average|
|Outbound Data Package Rate|N/A|pkts\_out|userId, clusterId, and role|Average|
|Outbound Data Package Rate|N/A|proc\_run|userId, clusterId, and role|Average|
|Total Process Number|N/A|proc\_total|userId, clusterId, and role|Average|
|Blocked Process Number|N/A|procs\_blocked|userId, clusterId, and role|Average|
|Created Process/ Process Number|N/A|procs\_created|userId, clusterId, and role|Average|
|RegionServer Put Request Latency|N/A|putRequestLatency\_mean|userId, clusterId, and role|Average|
|ritCount|N/A|ritCount|userId, clusterId, and role|Average|
|rs\_fullGC\_avg\_time|N/A|rs\_fullGC\_avg\_time|userId, clusterId, and role|Average|
|rs\_fullGC\_max\_time|N/A|rs\_fullGC\_max\_time|userId, clusterId, and role|Average|
|rs\_fullGC\_num\_ops|N/A|rs\_fullGC\_num\_ops|userId, clusterId, and role|Average|
|RegionServer RegionServer Handler Queue Size|N/A|rs\_handlerQueueSize|userId, clusterId, and role|Average|
|rs\_tcp\_count|N/A|rs\_tcp\_count|userId, clusterId, and role|Average|
|zookeeper\_tcp\_count|N/A|zookeeper\_tcp\_count|userId, clusterId, and role|Average|
|read data per second|byte/s|readDataPerSecondKB|userId, clusterId, and role|Average|
|write data per second|byte/s|writeDataPerSecondKB|userId, clusterId, and role|Average|
|Batch Put avg RT|ms|batchPutRequestLatency\_mean|userId, clusterId, and role|Average|
|above global memory upper limit write ops|count/s|AboveGlobalMemLimit\_num\_ops|userId, clusterId, and role|Average|
|Delete ops|count/s|DeleteRequestLatency\_num\_ops|userId, clusterId, and role|Average|
|system disk free percent|%|disk\_free\_percent\_rootfs|userId, clusterId, and role|Average|
|Get average RT|ms|GetRequestLatency\_mean|userId, clusterId, and role|Average|
|Get ops|count/s|GetRequestLatency\_num\_ops|userId, clusterId, and role|Average|
|Master call queue size|count|HandlerQueueSize|userId, clusterId, and role|Average|
|15 minutes avg load|1|load\_fifteen|userId, clusterId, and role|Average|
|5 minutes avg load|1|load\_five|userId, clusterId, and role|Average|
|load per minute|1|load\_one|userId, clusterId, and role|Average|
|memory free size|KB|mem\_free|userId, clusterId, and role|Average|
|memory total size|KB|mem\_total|userId, clusterId, and role|Average|
|mem free percent|Decimal number between 0 and 1|MemFreePercent|userId, clusterId, and role|Average|
|RS memstore size|byte|MemStoreSize|userId, clusterId, and role|Average|
|number of dead RS|count|NumDeadRegionServers|userId, clusterId, and role|Average|
|number of region servers|count|NumRegionServers|userId, clusterId, and role|Average|
|network packets in|count/s|pkts\_in|userId, clusterId, and role|Average|
|network packets out|count/s|pkts\_out|userId, clusterId, and role|Average|
|number of RUN processes\(threads\)|count|proc\_run|userId, clusterId, and role|Average|
|total number of processes\(threads\)|count|proc\_total|userId, clusterId, and role|Average|
|number of BLOCKED processes\(threads\)|count|procs\_blocked|userId, clusterId, and role|Average|
|number of processes\(threads\) created per second|count/s|procs\_created|userId, clusterId, and role|Average|
|put avg RT|ms|putRequestLatency\_mean|userId, clusterId, and role|Average|
|read avg RT|ms|ReadRequests\_avg\_time|userId, clusterId, and role|Average|
|read request ops|count/s|ReadRequests\_num\_ops|userId, clusterId, and role|Average|
|total regions|count|Regions|userId, clusterId, and role|Average|
|rit region count|count|ritCountOverThreshold|userId, clusterId, and role|Average|
|RS RPC handler queue heap size|byte|rs\_handlerQueueHeapSize|userId, clusterId, and role|Average|
|RS call queue size|count|rs\_handlerQueueSize|userId, clusterId, and role|Average, Maximum, and Minimum|
|write avg RT|ms|WriteRequests\_avg\_time|userId, clusterId, and role|Average|
|write request ops|count/s|WriteRequests\_num\_ops|userId, clusterId, and role|Average|
|Append avg rt|ms|Append\_Mean|userId, clusterId, and role|Average|

