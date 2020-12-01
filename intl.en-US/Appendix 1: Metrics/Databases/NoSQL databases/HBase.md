# HBase

This topic describes the metrics of ApsaraDB for HBase Standard Edition.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_hbase**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|above global memory upper limit write ops|CountSecond|AboveGlobalMemLimit\_num\_ops|userId, clusterId, and role|Average|
|ActiveApplications|N/A|ActiveApplications|userId, clusterId, and role|Average|
|AggregatecontainersAllocated|N/A|AggregatecontainersAllocated|userId, clusterId, and role|Average|
|AggregatecontainersReleased|N/A|AggregatecontainersReleased|userId, clusterId, and role|Average|
|active handler number|count|AliveHandlerNum|userId, clusterId, and role|Average|
|Append avg rt|Milliseconds|Append\_Mean|userId, clusterId, and role|Average|
|Append ops|CountSecond|Append\_num\_ops|userId, clusterId, and role|Average|
|AppsCompleted|N/A|AppsCompleted|userId, clusterId, and role|Average|
|AppsFailed|N/A|AppsFailed|userId, clusterId, and role|Average|
|AppsKilled|N/A|AppsKilled|userId, clusterId, and role|Average|
|AppsPending|N/A|AppsPending|userId, clusterId, and role|Average|
|AvailableMB|MB|AvailableMB|userId, clusterId, and role|Average|
|AvailableVCores|N/A|AvailableVCores|userId, clusterId, and role|Average|
|BlockCache access count|Count|BlockCacheCount|userId, clusterId, and role|Average|
|BlockCache hit percent|%|BlockCacheCountHitPercent|userId, clusterId, and role|Average|
|BlockCache evict count|Count|BlockCacheEvictedCount|userId, clusterId, and role|Average|
|BlockCacheExpressHitPercent|N/A|BlockCacheExpressHitPercent|userId, clusterId, and role|Average|
|BlockCache free size|Bytes|BlockCacheFree|userId, clusterId, and role|Average|
|BlockCache miss count|Count|BlockCacheMissCount|userId, clusterId, and role|Average|
|BlockCache current size|Bytes|BlockCacheSize|userId, clusterId, and role|Average|
|BlockCapacity|N/A|BlockCapacity|userId, clusterId, and role|Average|
|BlockChecksumOpAvgTime|N/A|BlockChecksumOpAvgTime|userId, clusterId, and role|Average|
|BlockChecksumOpNumOps|N/A|BlockChecksumOpNumOps|userId, clusterId, and role|Average|
|BlockReportsAvgTime|N/A|BlockReportsAvgTime|userId, clusterId, and role|Average|
|BlockVerificationFailures|N/A|BlockVerificationFailures|userId, clusterId, and role|Average|
|BlocksRead|N/A|BlocksRead|userId, clusterId, and role|Average|
|BlocksRemoved|N/A|BlocksRemoved|userId, clusterId, and role|Average|
|BlocksReplicated|N/A|BlocksReplicated|userId, clusterId, and role|Average|
|BlocksTotal|N/A|BlocksTotal|userId, clusterId, and role|Average|
|BlocksUncached|N/A|BlocksUncached|userId, clusterId, and role|Average|
|BlocksVerified|N/A|BlocksVerified|userId, clusterId, and role|Average|
|BlocksWritten|N/A|BlocksWritten|userId, clusterId, and role|Average|
|dn bytes read|Bytes/s|BytesRead|userId, clusterId, and role|Average|
|dn bytes written|Bytes/s|BytesWritten|userId, clusterId, and role|Average|
|rpc call queue length|Count|CallQueueLength|userId, clusterId, and role|Average|
|HDFS free bytes|Bytes|CapacityRemaining|userId, clusterId, and role|Average|
|HDFS total bytes|Bytes|CapacityTotal|userId, clusterId, and role|Average|
|HDFS used bytes|Bytes|CapacityUsed|userId, clusterId, and role|Average|
|HDFS non DFS used|Bytes|CapacityUsedNonDFS|userId, clusterId, and role|Average|
|HDFS used percent|0-1|CapacityUsedPercent|userId, clusterId, and role|Average|
|ClusterRequests|N/A|ClusterRequests|userId, clusterId, and role|Average|
|ContainersIniting|N/A|ContainersIniting|userId, clusterId, and role|Average|
|CopyBlockOpAvgTime|N/A|CopyBlockOpAvgTime|userId, clusterId, and role|Average|
|CopyBlockOpNumOps|N/A|CopyBlockOpNumOps|userId, clusterId, and role|Average|
|CorruptBlocks|N/A|CorruptBlocks|userId, clusterId, and role|Average|
|delete average RT|Milliseconds|DeleteRequestLatency\_mean|userId, clusterId, and role|Average|
|Delete ops|CountSecond|DeleteRequestLatency\_num\_ops|userId, clusterId, and role|Average|
|ExcessBlocks|N/A|ExcessBlocks|userId, clusterId, and role|Average|
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
|Get average RT|Milliseconds|GetRequestLatency\_mean|userId, clusterId, and role|Average|
|Get ops|CountSecond|GetRequestLatency\_num\_ops|userId, clusterId, and role|Average|
|HOFSAbortUploadException|N/A|HOFSAbortUploadException|userId, clusterId, and role|Average|
|HOFSConfigException|N/A|HOFSConfigException|userId, clusterId, and role|Average|
|HOFSTooManyFileReader|N/A|HOFSTooManyFileReader|userId, clusterId, and role|Average|
|Master call queue size|Count|HandlerQueueSize|userId, clusterId, and role|Average|
|HlogCount|N/A|HlogCount|userId, clusterId, and role|Average|
|HlogFileSize|N/A|HlogFileSize|userId, clusterId, and role|Average|
|HlogWriteLatency\_avg\_time|N/A|HlogWriteLatency\_avg\_time|userId, clusterId, and role|Average|
|HlogWriteLatency\_num\_ops|N/A|HlogWriteLatency\_num\_ops|userId, clusterId, and role|Average|
|HlogWriteSize\_avg\_time|N/A|HlogWriteSize\_avg\_time|userId, clusterId, and role|Average|
|HlogWriteSize\_num\_ops|N/A|HlogWriteSize\_num\_ops|userId, clusterId, and role|Average|
|LoadPerCpu|N/A|LoadPerCpu|userId, clusterId, and role|Average|
|MaxRegionSize|N/A|MaxRegionSize|userId, clusterId, and role|Average|
|mem free percent|0-1|MemFreePercent|userId, clusterId, and role|Average|
|MemHeapCommittedM|N/A|MemHeapCommittedM|userId, clusterId, and role|Average|
|MemHeapMaxM|N/A|MemHeapMaxM|userId, clusterId, and role|Average|
|MemHeapUsedM|N/A|MemHeapUsedM|userId, clusterId, and role|Average|
|MemMaxM|N/A|MemMaxM|userId, clusterId, and role|Average|
|MemNonHeapCommittedM|N/A|MemNonHeapCommittedM|userId, clusterId, and role|Average|
|MemNonHeapMaxM|N/A|MemNonHeapMaxM|userId, clusterId, and role|Average|
|MemNonHeapUsedM|N/A|MemNonHeapUsedM|userId, clusterId, and role|Average|
|RS memstore size|Bytes|MemStoreSize|userId, clusterId, and role| |
|MissingBlocks|N/A|MissingBlocks|userId, clusterId, and role|Average|
|MutationsWithoutWALCount|N/A|MutationsWithoutWALCount|userId, clusterId, and role|Average|
|MutationsWithoutWALSize|N/A|MutationsWithoutWALSize|userId, clusterId, and role|Average|
|NotServeringRegionEXception|N/A|NotServeringRegionEXception|userId, clusterId, and role|Average|
|NumOpenConnections|N/A|NumOpenConnections|userId, clusterId, and role|Average|
|number of dead RS|Count|NumDeadRegionServers|userId, clusterId, and role|Average|
|number of region servers|Count|NumRegionServers|userId, clusterId, and role|Average|
|OutOfOrderScannerNextException|N/A|OutOfOrderScannerNextException|userId, clusterId, and role|Average|
|PendingDataNodeMessageCount|N/A|PendingDataNodeMessageCount|userId, clusterId, and role|Average|
|PendingDeletionBlocks|N/A|PendingDeletionBlocks|userId, clusterId, and role|Average|
|PendingReplicationBlocks|N/A|PendingReplicationBlocks|userId, clusterId, and role|Average|
|PercentFilesLocalSecondaryRegions|N/A|PercentFilesLocalSecondaryRegions|userId, clusterId, and role|Average|
|PostponedMisreplicatedBlocks|N/A|PostponedMisreplicatedBlocks|userId, clusterId, and role|Average|
|ReadBlockOpAvgTime|N/A|ReadBlockOpAvgTime|userId, clusterId, and role|Average|
|ReadBlockOpNumOps|N/A|ReadBlockOpNumOps|userId, clusterId, and role|Average|
|read avg RT|Milliseconds|ReadRequests\_avg\_time|userId, clusterId, and role|Average|
|read request ops|CountSecond|ReadRequests\_num\_ops|userId, clusterId, and role|Average|
|ReceivedBytes|N/A|ReceivedBytes|userId, clusterId, and role|Average|
|RegionMovedException|N/A|RegionMovedException|userId, clusterId, and role|Average|
|RegionServerStartTime|N/A|RegionServerStartTime|userId, clusterId, and role|Average|
|RegionServer\_NumOpenConnections|N/A|RegionServer\_NumOpenConnections|userId, clusterId, and role|Average|
|RegionSplitTime\_avg\_time|N/A|RegionSplitTime\_avg\_time|userId, clusterId, and role|Average|
|RegionSplitTime\_num\_ops|N/A|RegionSplitTime\_num\_ops|userId, clusterId, and role|Average|
|RegionTooBusyException|N/A|RegionTooBusyException|userId, clusterId, and role|Average|
|total regions|Count|Regions|userId, clusterId, and role|Average|
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
|write avg RT|Milliseconds|WriteRequests\_avg\_time|userId, clusterId, and role|Average|
|write request ops|CountSecond|WriteRequests\_num\_ops|userId, clusterId, and role|Average|
|Batch Put avg RT|Nanoseconds|batchPutRequestLatency\_mean|userId, clusterId, and role|Average|
|network flow in|Bytes/s|Bytes\_in|userId, clusterId, and role|Average|
|network flow out|Bytes/s|Bytes\_out|userId, clusterId, and role|Average|
|compaction queue size|Count|compactionQueueSize|userId, clusterId, and role|Average, Maximum, and Minimum|
|CPU idle|%|cpu\_idle|userId, clusterId, and role|Average, Maximum, and Minimum|
|CPU system|%|cpu\_system|userId, clusterId, and role|Average|
|CPU user|%|cpu\_user|userId, clusterId, and role|Average|
|system disk free percent|%|disk\_free\_percent\_rootfs|userId, clusterId, and role|Average|
|Free Disk Size|The domain name of the site to be monitored.|disk\_total|userId, clusterId, and role|Average|
|system disk free percent|N/A|disk\_free\_percent\_rootfs|userId, clusterId, and role|Average|
|Total Disk Size|N/A|disk\_total|userId, clusterId, and role|Average|
|15 minutes avg load|N/A|load\_fifteen|userId, clusterId, and role|Average|
|5 minutes avg load|N/A|load\_five|userId, clusterId, and role|Average|
|load per minute|N/A|load\_one|userId, clusterId, and role|Average|
|memory free size|N/A|mem\_free|userId, clusterId, and role|Average|
|memory total size|N/A|mem\_total|userId, clusterId, and role|Average|
|NumCallsInPriorityQueue|N/A|numCallsInPriorityQueue|userId, clusterId, and role|Average|
|NumCallsInReplicationQueue|N/A|NumCallsInReplicationQueue|userId, clusterId, and role|Average|
|network packets in|CountSecond|pkts\_in|userId, clusterId, and role|Average|
|network packets out|CountSecond|pkts\_out|userId, clusterId, and role|Average|
|total number of processes \(threads\)|Count|proc\_total|userId, clusterId, and role|Average|
|number of BLOCKED processes \(threads\)|Count|procs\_blocked|userId, clusterId, and role|Average|
|number of processes \(threads\) created per second|CountSecond|procs\_created|userId, clusterId, and role|Average|
|put avg RT|Nanoseconds|putRequestLatency\_mean|userId, clusterId, and role|Average|
|read data per second|Bytes/s|readDataPerSecondKB|userId, clusterId, and role|Average|
|rit region count|Count|ritCountOverThreshold|userId, clusterId, and role|Average|
|ritCount|N/A|ritCount|userId, clusterId, and role|Average|
|rs\_fullGC\_max\_time|N/A|rs\_fullGC\_max\_time|userId, clusterId, and role|Average|
|rs\_fullGC\_num\_ops|N/A|rs\_fullGC\_num\_ops|userId, clusterId, and role|Average|
|rs\_tcp\_count|N/A|rs\_tcp\_count|userId, clusterId, and role|Average|
|RS RPC handler queue heap size|Bytes|rs\_handlerQueueHeapSize|userId, clusterId, and role|Average|
|RS call queue size|Count|rs\_handlerQueueSize|userId, clusterId, and role|Average, Maximum, and Minimum|
|zookeeper\_tcp\_count|N/A|zookeeper\_tcp\_count|userId, clusterId, and role|Average|
|number of RUN processes \(threads\)|Count|proc\_run|userId, clusterId, and role|Average|
|BlockReportsNumOps|N/A|BlockReportsNumOps|userId, clusterId, and role|Average|

