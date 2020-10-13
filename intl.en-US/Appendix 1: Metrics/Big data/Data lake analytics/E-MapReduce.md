# E-MapReduce

This topic describes the metrics for E-MapReduce.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for ApsaraDB for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_emr**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|ActiveApplications|N/A|ActiveApplications|userId, clusterId, and role|Average|
|ActiveUsers|N/A|ActiveUsers|userId, clusterId, and role|Average|
|AggregateContainersAllocated|N/A|AggregateContainersAllocated|userId, clusterId, and role|Average|
|AggregateContainersReleased|N/A|AggregateContainersReleased|userId, clusterId, and role|Average|
|AllocatedContainers|N/A|AllocatedContainers|userId, clusterId, and role|Average|
|AppsCompleted|N/A|AppsCompleted|userId, clusterId, and role|Average|
|AppsFailed|N/A|AppsFailed|userId, clusterId, and role|Average|
|AppsKilled|N/A|AppsKilled|userId, clusterId, and role|Average|
|AppsPending|N/A|AppsPending|userId, clusterId, and role|Average|
|AppsRunning|N/A|AppsRunning|userId, clusterId, and role|Average|
|AppsSubmitted|N/A|AppsSubmitted|userId, clusterId, and role|Average|
|AvailableMB|N/A|AvailableMB|userId, clusterId, and role|Average|
|AvailableVCores|N/A|AvailableVCores|userId, clusterId, and role|Average|
|BlockCapacity|N/A|BlockCapacity|userId, clusterId, and role|Average|
|BlockChecksumOpAvgTime|ms|BlockChecksumOpAvgTime|userId, clusterId, and role|Average|
|BlockChecksumOpNumOps|N/A|BlockChecksumOpNumOps|userId, clusterId, and role|Average|
|BlockReportsAvgTime|ms|BlockReportsAvgTime|userId, clusterId, and role|Average|
|BlockReportsNumOps|N/A|BlockReportsNumOps|userId, clusterId, and role|Average|
|BlockVerificationFailures|N/A|BlockVerificationFailures|userId, clusterId, and role|Average|
|BlocksRead|N/A|BlocksRead|userId, clusterId, and role|Average|
|BlocksRemoved|N/A|BlocksRemoved|userId, clusterId, and role|Average|
|BlocksReplicated|N/A|BlocksReplicated|userId, clusterId, and role|Average|
|BlocksTotal|N/A|BlocksTotal|userId, clusterId, and role|Average|
|BlocksUncached|N/A|BlocksUncached|userId, clusterId, and role|Average|
|BlocksVerified|N/A|BlocksVerified|userId, clusterId, and role|Average|
|BlocksWritten|N/A|BlocksWritten|userId, clusterId, and role|Average|
|BytesRead|Byte|BytesRead|userId, clusterId, and role|Average|
|BytesWritten|Byte|BytesWritten|userId, clusterId, and role|Average|
|CallQueueLength|N/A|CallQueueLength|userId, clusterId, and role|Average|
|CapacityRemaining|N/A|CapacityRemaining|userId, clusterId, and role|Average|
|CapacityTotal|N/A|CapacityTotal|userId, clusterId, and role|Average|
|CapacityUsed|N/A|CapacityUsed|userId, clusterId, and role|Average|
|CapacityUsedNonDFS|N/A|CapacityUsedNonDFS|userId, clusterId, and role|Average|
|ContainersCompleted|N/A|ContainersCompleted|userId, clusterId, and role|Average|
|ContainersFailed|N/A|ContainersFailed|userId, clusterId, and role|Average|
|ContainersIniting|N/A|ContainersIniting|userId, clusterId, and role|Average|
|ContainersKilled|N/A|ContainersKilled|userId, clusterId, and role|Average|
|ContainersLaunched|N/A|ContainersLaunched|userId, clusterId, and role|Average|
|ContainersRunning|N/A|ContainersRunning|userId, clusterId, and role|Average|
|CopyBlockOpAvgTime|ms|CopyBlockOpAvgTime|userId, clusterId, and role|Average|
|CopyBlockOpNumOps|N/A|CopyBlockOpNumOps|userId, clusterId, and role|Average|
|CorruptBlocks|N/A|CorruptBlocks|userId, clusterId, and role|Average|
|DataNodeDfsUsedPercent|%|DataNodeDfsUsedPercent|userId, clusterId, and role|Average, Maximum, and Minimum|
|DataNodeHttpPortOpen|N/A|DataNodeHttpPortOpen|userId, clusterId, and role|Average|
|DataNodeIpcPortOpen|N/A|DataNodeIpcPortOpen|userId, clusterId, and role|Average|
|DataNodePortOpen|N/A|DataNodePortOpen|userId, clusterId, and role|Average|
|ExcessBlocks|N/A|ExcessBlocks|userId, clusterId, and role|Average|
|ExpiredHeartbeats|N/A|ExpiredHeartbeats|userId, clusterId, and role|Average|
|Fetch.LocalTimeMs.max|N/A|Fetch.LocalTimeMs.max|userId, clusterId, and role|Average|
|Fetch.LocalTimeMs.mean|N/A|Fetch.LocalTimeMs.mean|userId, clusterId, and role|Average|
|Fetch.LocalTimesMs.stddev|N/A|Fetch.LocalTimesMs.stddev|userId, clusterId, and role|Average|
|Fetch.RemoteTimeMs.max|N/A|Fetch.RemoteTimeMs.max|userId, clusterId, and role|Average|
|Fetch.RemoteTimeMs.mean|N/A|Fetch.RemoteTimeMs.mean|userId, clusterId, and role|Average|
|Fetch.RemoteTimeMs.stddev|N/A|Fetch.RemoteTimeMs.stddev|userId, clusterId, and role|Average|
|Fetch.RequestQueueTimeMs.max|N/A|Fetch.RequestQueueTimeMs.max|userId, clusterId, and role|Average|
|Fetch.RequestQueueTimeMs.mean|N/A|Fetch.RequestQueueTimeMs.mean|userId, clusterId, and role|Average|
|Fetch.RequestQueueTimeMs.stddev|N/A|Fetch.RequestQueueTimeMs.stddev|userId, clusterId, and role|Average|
|Fetch.ResponseQueueTimeMs.max|N/A|Fetch.ResponseQueueTimeMs.max|userId, clusterId, and role|Average|
|Fetch.ResponseQueueTimeMs.mean|N/A|Fetch.ResponseQueueTimeMs.mean|userId, clusterId, and role|Average|
|Fetch.ResponseQueueTimeMs.stddev|N/A|Fetch.ResponseQueueTimeMs.stddev|userId, clusterId, and role|Average|
|Fetch.ResponseSendTimeMs.max|N/A|Fetch.ResponseSendTimeMs.max|userId, clusterId, and role|Average|
|Fetch.ResponseSendTimeMs.mean|N/A|Fetch.ResponseSendTimeMs.mean|userId, clusterId, and role|Average|
|Fetch.ResponseSendTimeMs.stddev|N/A|Fetch.ResponseSendTimeMs.stddev|userId, clusterId, and role|Average|
|Fetch.ThrottleTimeMs.max|N/A|Fetch.ThrottleTimeMs.max|userId, clusterId, and role|Average|
|Fetch.ThrottleTimeMs.mean|N/A|Fetch.ThrottleTimeMs.mean|userId, clusterId, and role|Average|
|Fetch.ThrottleTimeMs.stddev|N/A|Fetch.ThrottleTimeMs.stddev|userId, clusterId, and role|Average|
|Fetch.TotalTimeMs.max|N/A|Fetch.TotalTimeMs.max|userId, clusterId, and role|Average|
|Fetch.TotalTimeMs.mean|N/A|Fetch.TotalTimeMs.mean|userId, clusterId, and role|Average|
|Fetch.TotalTimeMs.stddev|N/A|Fetch.TotalTimeMs.stddev|userId, clusterId, and role|Average|
|FlushNanosAvgTime|ns|FlushNanosAvgTime|userId, clusterId, and role|Average|
|FlushNanosNumOps|ns|FlushNanosNumOps|userId, clusterId, and role|Average|
|FsyncCount|N/A|FsyncCount|userId, clusterId, and role|Average|
|GcCount|N/A|GcCount|userId, clusterId, and role|Average|
|GcTimeMillis|ms|GcTimeMillis|userId, clusterId, and role|Average|
|HMasterHttpPortOpen|N/A|HMasterHttpPortOpen|userId, clusterId, and role|Average|
|HMasterIpcPortOpen|N/A|HMasterIpcPortOpen|userId, clusterId, and role|Average|
|HMasterJmxPortOpen|N/A|HMasterJmxPortOpen|userId, clusterId, and role|Average|
|HRegionServerHttpPortOpen|N/A|HRegionServerHttpPortOpen|userId, clusterId, and role|Average|
|HRegionServerIpcPortOpen|N/A|HRegionServerIpcPortOpen|userId, clusterId, and role|Average|
|HRegionServerJmxPortOpen|N/A|HRegionServerJmxPortOpen|userId, clusterId, and role|Average|
|HiveServer2PortOpen|N/A|HiveServer1PortOpen|userId, clusterId, and role|Average|
|HiveServer2WebuiPortOpen|N/A|HiveServer1WebuiPortOpen|userId, clusterId, and role|Average|
|HuePortOpen|N/A|HuePortOpen|userId, clusterId, and role|Average|
|JobHistoryPortOpen|N/A|JobHistoryPortOpen|userId, clusterId, and role|Average|
|JobHistoryWebappPortOpen|N/A|JobHistoryWebappPortOpen|userId, clusterId, and role|Average|
|JournalNodeHttpPortOpen|N/A|JournalNodeHttpPortOpen|userId, clusterId, and role|Average|
|JournalNodeRpcPortOpen|N/A|JournalNodeRpcPortOpen|userId, clusterId, and role|Average|
|KafkaActiveControllerCount|N/A|KafkaActiveControllerCount|userId, clusterId, and role|Average|
|KafkaBrokerTopicMetricBytesInPerSec1MinuteRate|N/A|KafkaBrokerTopicMetricBytesInPerSec0MinuteRate|userId, clusterId, and role|Average|
|KafkaBrokerTopicMetricBytesInPerSecCount|N/A|KafkaBrokerTopicMetricBytesInPerSecCount|userId, clusterId, and role|Average|
|KafkaBrokerTopicMetricBytesOutPerSec1MinuteRate|N/A|KafkaBrokerTopicMetricBytesOutPerSec0MinuteRate|userId, clusterId, and role|Average|
|KafkaBrokerTopicMetricBytesOutPerSecCount|N/A|KafkaBrokerTopicMetricBytesOutPerSecCount|userId, clusterId, and role|Average|
|KafkaBrokerTopicMetricBytesRejectedPerSec1MinuteRate|N/A|KafkaBrokerTopicMetricBytesRejectedPerSec0MinuteRate|userId, clusterId, and role|Average|
|KafkaBrokerTopicMetricRejectPerSecCount|N/A|KafkaBrokerTopicMetricRejectPerSecCount|userId, clusterId, and role|Average|
|KafkaBrokerTopicMetricFailedFetchRequestsPerSec1MinuteRate|N/A|KafkaBrokerTopicMetricFailedFetchRequestsPerSec0MinuteRate|userId, clusterId, and role|Average|
|KafkaBrokerTopicMetricFailedFetchRequestsPerSecCount|N/A|KafkaBrokerTopicMetricFailedFetchRequestsPerSecCount|userId, clusterId, and role|Average|
|KafkaBrokerTopicMetricFailedProduceRequestsPerSec1MinuteRate|N/A|KafkaBrokerTopicMetricFailedProduceRequestsPerSec0MinuteRate|userId, clusterId, and role|Average|
|KafkaBrokerTopicMetricFailedProduceRequestsPerSecCount|N/A|KafkaBrokerTopicMetricFailedProduceRequestsPerSecCount|userId, clusterId, and role|Average|
|KafkaBrokerTopicMetricMessagesInPerSec1MinuteRate|N/A|KafkaBrokerTopicMetricMessagesInPerSec0MinuteRate|userId, clusterId, and role|Average|
|KafkaBrokerTopicMetricMessagesIPerSecCount|N/A|KafkaBrokerTopicMetricMessagesIPerSecCount|userId, clusterId, and role|Average|
|KafkaBrokerTopicMetricTotalFetchRequestsPerSec1MinuteRate|N/A|KafkaBrokerTopicMetricTotalFetchRequestsPerSec0MinuteRate|userId, clusterId, and role|Average|
|KafkaBrokerTopicMetricTotalFetchRequestsPerSecCount|N/A|KafkaBrokerTopicMetricTotalFetchRequestsPerSecCount|userId, clusterId, and role|Average|
|KafkaBrokerTopicMetricTotalProduceRequestsPerSec1MinuteRate|N/A|KafkaBrokerTopicMetricTotalProduceRequestsPerSec0MinuteRate|userId, clusterId, and role|Average|
|KafkaBrokerTopicMetricTotalProduceRequestsPerSecCount|N/A|KafkaBrokerTopicMetricTotalProduceRequestsPerSecCount|userId, clusterId, and role|Average|
|KafkaBytesRejectedPerSec1MinuteRate|N/A|KafkaBytesRejectedPerSec0MinuteRate|userId, clusterId, and role|Average|
|KafkaCleanerIo1MinuteRate|N/A|KafkaCleanerIo0MinuteRate|userId, clusterId, and role|Average|
|KafkaCleanerIoCount|N/A|KafkaCleanerIoCount|userId, clusterId, and role|Average|
|KafkaDiskUsageMaxPercent|N/A|KafkaDiskUsageMaxPercent|userId, clusterId, and role|Average|
|KafkaDiskUsageStddevPercent|N/A|KafkaDiskUsageStddevPercent|userId, clusterId, and role|Average|
|KafkaGroupMetadataManagerNumGroups|N/A|KafkaGroupMetadataManagerNumGroups|userId, clusterId, and role|Average|
|KafkaGroupMetadataManagerNumOffsets|N/A|KafkaGroupMetadataManagerNumOffsets|userId, clusterId, and role|Average|
|KafkalsrEpandsPerSec1MinuteRate|N/A|KafkalsrEpandsPerSec0MinuteRate|userId, clusterId, and role|Average|
|KafkaLsrEpandsPerSecCount|N/A|KafkaLsrEpandsPerSecCount|userId, clusterId, and role|Average|
|KafkaLsrShrinksPerSec1MinuteRate|N/A|KafkaLsrShrinksPerSec0MinuteRate|userId, clusterId, and role|Average|
|KafkaLsrShrinksPerSecCount|N/A|KafkaLsrShrinksPerSecCount|userId, clusterId, and role|Average|
|KafkaLeaderElectionRateAndTimeMs1MinuteRate|N/A|KafkaLeaderElectionRateAndTimeMs0MinuteRate|userId, clusterId, and role|Average|
|KafkaLeaderElectionRateAndTimeMsCount|N/A|KafkaLeaderElectionRateAndTimeMsCount|userId, clusterId, and role|Average|
|KafkaLeaderElectionRateAndTimeMsMax|N/A|KafkaLeaderElectionRateAndTimeMsMax|userId, clusterId, and role|Average|
|KafkaLeaderElectionRateAndTimeMsMean|N/A|KafkaLeaderElectionRateAndTimeMsMean|userId, clusterId, and role|Average|
|KafkaLeaderElectionRateAndTimeMsMaxRate|N/A|KafkaLeaderElectionRateAndTimeMsMaxRate|userId, clusterId, and role|Average|
|KafkaLeaderElectionRateAndTimeMsMedian|N/A|KafkaLeaderElectionRateAndTimeMsMedian|userId, clusterId, and role|Average|
|KafkaLeaderElectionRateAndTimeMsMin|N/A|KafkaLeaderElectionRateAndTimeMsMin|userId, clusterId, and role|Average|
|KafkaLeaderElectionRateAndTimeMsStddev|N/A|KafkaLeaderElectionRateAndTimeMsStddev|userId, clusterId, and role|Average|
|KafkaLogCleanerMaxBufferUtilPercent|N/A|KafkaLogCleanerMaxBufferUtilPercent|userId, clusterId, and role|Average|
|KafkaLogCleanerMaxCleanTime|N/A|KafkaLogCleanerMaxCleanTime|userId, clusterId, and role|Average|
|KafkaLogCleanerMaxDirtyPercent|N/A|KafkaLogCleanerMaxDirtyPercent|userId, clusterId, and role|Average|
|KafkaLogCleanerRecopyPercent|N/A|KafkaLogCleanerRecopyPercent|userId, clusterId, and role|Average|
|KafkaLogFlush1MinuteRate|N/A|KafkaLogFlush0MinuteRate|userId, clusterId, and role|Average|
|KafkaLogFlushCount|N/A|KafkaLogFlushCount|userId, clusterId, and role|Average|
|KafkaLogFlushRateAndTimeMsMax|N/A|KafkaLogFlushRateAndTimeMsMax|userId, clusterId, and role|Average|
|KafkaLogFlushRateAndTimeMsMean|N/A|KafkaLogFlushRateAndTimeMsMean|userId, clusterId, and role|Average|
|KafkaLogFlushRateAndTimeMsMeanRate|N/A|KafkaLogFlushRateAndTimeMsMeanRate|userId, clusterId, and role|Average|
|KafkaLogFlushRateAndTimeMsMidean|N/A|KafkaLogFlushRateAndTimeMsMidean|userId, clusterId, and role|Average|
|KafkaLogFlushRateAndAndTimeMsMin|N/A|KafkaLogFlushRateAndAndTimeMsMin|userId, clusterId, and role|Average|
|KafkaLogFlushRateAndAndTimeMsStddev|N/A|KafkaLogFlushRateAndAndTimeMsStddev|userId, clusterId, and role|Average|
|KafkaNetworkProcessorAvgIdlePercent|N/A|KafkaNetworkProcessorAvgIdlePercent|userId, clusterId, and role|Average|
|KafkaOfflineLogDirectoryCount|Count|KafkaOfflineLogDirectoryCount|userId, clusterId, and role|Average|
|KafkaOfflinePartitionsCount|N/A|KafkaOfflinePartitionsCount|userId, clusterId, and role|Average|
|KafkaOfflineReplicaCount|Count|KafkaOfflineReplicaCount|userId, clusterId, and role|Average|
|KafkaPreferredReplicaImbalanceCount|N/A|KafkaPreferredReplicaImbalanceCount|userId, clusterId, and role|Average|
|KafkaReplicaManagerDiskUsageMax|%|KafkaReplicaManagerDiskUsageMax|userId, clusterId, and role|Average|
|KafkaReplicaManagerDiskUsageMean|%|KafkaReplicaManagerDiskUsageMean|userId, clusterId, and role|Average|
|KafkaReplicaManagerDiskUsageStddev|%|KafkaReplicaManagerDiskUsageStddev|userId, clusterId, and role|Average|
|KafkaReplicaManagerLeaderCount|%|KafkaReplicaManagerLeaderCount|userId, clusterId, and role|Average|
|KafkaReplicaManagerPartitionCount|N/A|KafkaReplicaManagerPartitionCount|userId, clusterId, and role|Average|
|KafkaReplicaManagerUnderReplicatedPartitions|N/A|KafkaReplicaManagerUnderReplicatedPartitions|userId, clusterId, and role|Average|
|KafkaRequestHandlerAvgIdlePercent1MinuteRate|N/A|KafkaRequestHandlerAvgIdlePercent0MinuteRate|userId, clusterId, and role|Average|
|KafkaRequestHandlerAvgIdlePercentCount|N/A|KafkaRequestHandlerAvgIdlePercentCount|userId, clusterId, and role|Average|
|KafkaRequestQueueSize|N/A|KafkaRequestQueueSize|userId, clusterId, and role|Average|
|KafkaResponseQueueSize|N/A|KafkaResponseQueueSize|userId, clusterId, and role|Average|
|KafkaUncleanLeaderElectionsPerSec1MinuteRate|N/A|KafkaUncleanLeaderElectionsPerSec0MinuteRate|userId, clusterId, and role|Average|
|KafkaUncleanLeaderElectionsPerSecCount|N/A|KafkaUncleanLeaderElectionsPerSecCount|userId, clusterId, and role|Average|
|KafkaUnderReplicatedPartitions|N/A|KafkaUnderReplicatedPartitions|userId, clusterId, and role|Average|
|KafkaZookeeperAuthFailuresPerSec1MinuteRate|N/A|KafkaZookeeperAuthFailuresPerSec0MinuteRate|userId, clusterId, and role|Average|
|KafkaZookeeperAuthFailuresPerSecCount|N/A|KafkaZookeeperAuthFailuresPerSecCount|userId, clusterId, and role|Average|
|KafkaZookeeperDisconnectionsPerSec1MinuteRat|N/A|KafkaZookeeperDisconnectionsPerSec0MinuteRat|userId, clusterId, and role|Average|
|KafkaZookeeperDisconnectionsPerSecCount|N/A|KafkaZookeeperDisconnectionsPerSecCount|userId, clusterId, and role|Average|
|KafkaZookeeperExpiresPerSec1MinuteRate|N/A|KafkaZookeeperExpiresPerSec0MinuteRate|userId, clusterId, and role|Average|
|KafkaZookeeperExpiresPerSecCount|N/A|KafkaZookeeperExpiresPerSecCount|userId, clusterId, and role|Average|
|KafkaZookeeperReadOnlyConnectionsPerSec1MinuteRate|N/A|KafkaZookeeperReadOnlyConnectionsPerSec0MinuteRate|userId, clusterId, and role|Average|
|KafkaZookeeperReadOnlyConnectionsPerSecCount|N/A|KafkaZookeeperReadOnlyConnectionsPerSecCount|userId, clusterId, and role|Average|
|KafkaZookeeperSaslAuthenticationsPerSec1MinuteRate|N/A|KafkaZookeeperSaslAuthenticationsPerSec0MinuteRate|userId, clusterId, and role|Average|
|KafkaZookeeperSaslAuthenticationsPerSecCount|N/A|KafkaZookeeperSaslAuthenticationsPerSecCount|userId, clusterId, and role|Average|
|KafkaZookeeperSyncConnectionsPerSec1MinuteRate|N/A|KafkaZookeeperSyncConnectionsPerSec0MinuteRate|userId, clusterId, and role|Average|
|KafkaZookeeperSyncConnectionsPerSecCount|N/A|KafkaZookeeperSyncConnectionsPerSecCount|userId, clusterId, and role|Average|
|MaxDFSUsedPercent|N/A|MaxDFSUsedPercent|userId, clusterId, and role|Average|
|MemHeapCommittedM|byte|MemHeapCommittedM|userId, clusterId, and role|Average|
|MemHeapMaxM|byte|MemHeapMaxM|userId, clusterId, and role|Average|
|MemHeapUsedM|byte|MemHeapUsedM|userId, clusterId, and role|Average|
|MemMaxM|byte|MemMaxM|userId, clusterId, and role|Average|
|MemNonHeapCommittedM|byte|MemNonHeapCommittedM|userId, clusterId, and role|Average|
|MemNonHeapMaxM|byte|MemNonHeapMaxM|userId, clusterId, and role|Average|
|MemNonHeapMaxM\_original|N/A|MemNonHeapMaxM\_original|userId, clusterId, and role|Average|
|MemNonHeapUsedM|byte|MemNonHeapUsedM|userId, clusterId, and role|Average|
|MemNonHeapUsedM\_original|N/A|MemNonHeapUsedM\_original|userId, clusterId, and role|Average|
|MemUsedPercent|N/A|MemUsedPercent|userId, clusterId, and role|Average|
|MetastorePortOpen|N/A|MetastorePortOpen|userId, clusterId, and role|Average|
|MissingBlocks|N/A|MissingBlocks|userId, clusterId, and role|Average|
|NameNodeActive|N/A|NameNodeActive|userId, clusterId, and role|Average|
|NameNodeHttpPortOpen|N/A|NameNodeHttpPortOpen|userId, clusterId, and role|Average|
|NameNodeSafeMode|N/A|NameNodeSafeMode|userId, clusterId, and role|Average|
|NameNodeIpcPortOpen|N/A|NameNodeIpcPortOpen|userId, clusterId, and role|Average|
|NetworkProcessorAvgIdlePercent|N/A|NetworkProcessorAvgIdlePercent|userId, clusterId, and role|Average|
|NodeManagerHttpPortOpen|N/A|NodeManagerHttpPortOpen|userId, clusterId, and role|Average|
|NodeManager\_AllocatedContainers|N/A|NodeManager\_AllocatedContainers|userId, clusterId, and role|Average|
|NumActiveNMs|N/A|NumActiveNMs|userId, clusterId, and role|Average|
|NumDeadDateNode|N/A|NumDeadDateNode|userId, clusterId, and role|Average|
|NumDecommissionedNMs|N/A|NumDecommissionedNMs|userId, clusterId, and role|Average|
|NumOpenConnections|N/A|NumOpenConnections|userId, clusterId, and role|Average|
|NumRebootedNMs|N/A|NumRebootedNMs|userId, clusterId, and role|Average|
|NumUnhealthyNMs|N/A|NumUnhealthyNMs|userId, clusterId, and role|Average|
|OozieAdminPortOpen|N/A|OozieAdminPortOpen|userId, clusterId, and role|Average|
|OozieHttpPortOpen|N/A|OozieHttpPortOpen|userId, clusterId, and role|Average|
|PartitionMaxAwait|N/A|PartitionMaxAwait|userId, clusterId, and role|Average|
|PartitionMaxUtilization|N/A|PartitionMaxUtilization|userId, clusterId, and role|Average|
|PendingContainers|N/A|PendingContainers|userId, clusterId, and role|Average|
|PendingDataNodeMessageCount|N/A|PendingDataNodeMessageCount|userId, clusterId, and role|Average|
|PendingDeletionBlocks|N/A|PendingDeletionBlocks|userId, clusterId, and role|Average|
|PendingReplicationBlocks|N/A|PendingReplicationBlocks|userId, clusterId, and role|Average|
|PostponedMisrelicatedBlocks|N/A|PostponedMisrelicatedBlocks|userId, clusterId, and role|Average|
|PrestoMasterHttpPortOpen|N/A|PrestoMasterHttpPortOpen|userId, clusterId, and role|Average|
|PrestoWorkerHttpPortOpen|N/A|PrestoWorkerHttpPortOpen|userId, clusterId, and role|Average|
|Produce.LocalTimeMs.max|N/A|Produce.LocalTimeMs.max|userId, clusterId, and role|Average|
|Produce.LocalTimeMs.mean|N/A|Produce.LocalTimeMs.mean|userId, clusterId, and role|Average|
|Produce.LocalTimeMs.stddev|N/A|Produce.LocalTimeMs.stddev|userId, clusterId, and role|Average|
|Produce.RemoteTimeMs.max|N/A|Produce.RemoteTimeMs.max|userId, clusterId, and role|Average|
|Produce.RemoteTimeMs.mean|N/A|Produce.RemoteTimeMs.mean|userId, clusterId, and role|Average|
|Produce.RemoteTimeMs.stddev|N/A|Produce.RemoteTimeMs.stddev|userId, clusterId, and role|Average|
|Produce.RequestQueueTimeMs.max|N/A|Produce.RequestQueueTimeMs.max|userId, clusterId, and role|Average|
|Produce.RequestQueueTimeMs.mean|N/A|Produce.RequestQueueTimeMs.mean|userId, clusterId, and role|Average|
|Produce.RequestQueueTimeMs.stddev|N/A|Produce.RequestQueueTimeMs.stddev|userId, clusterId, and role|Average|
|Produce.ResponseQueueTimeMs.max|N/A|Produce.ResponseQueueTimeMs.max|userId, clusterId, and role|Average|
|Produce.ResponseQueueTimeMs.mean|N/A|Produce.ResponseQueueTimeMs.mean|userId, clusterId, and role|Average|
|Produce.ResponseQueueTimeMs.stddev|N/A|Produce.ResponseQueueTimeMs.stddev|userId, clusterId, and role|Average|
|Produce.ResponseSendTimeMs.max|N/A|Produce.ResponseSendTimeMs.max|userId, clusterId, and role|Average|
|Produce.ResponseSendTimeMs.mean|N/A|Produce.ResponseSendTimeMs.mean|userId, clusterId, and role|Average|
|Produce.ResponseSendTimeMs.stddev|N/A|Produce.ResponseSendTimeMs.stddev|userId, clusterId, and role|Average|
|Produce.ThrottleTimeMs.max|N/A|Produce.ThrottleTimeMs.max|userId, clusterId, and role|Average|
|Produce.ThrottleTimeMs.mean|N/A|Produce.ThrottleTimeMs.mean|userId, clusterId, and role|Average|
|Produce.ThrottleTimeMs.stddev|N/A|Produce.ThrottleTimeMs.stddev|userId, clusterId, and role|Average|
|Produce.TotalTimeMs.max|N/A|Produce.TotalTimeMs.max|userId, clusterId, and role|Average|
|Produce.TotalTimeMs.mean|N/A|Produce.TotalTimeMs.mean|userId, clusterId, and role|Average|
|Produce.TotalTimeMs.stddev|N/A|Produce.TotalTimeMs.stddev|userId, clusterId, and role|Average|
|ProxyServerPortOpen|N/A|ProxyServerPortOpen|userId, clusterId, and role|Average|
|ReadBlockOpAvgTime|ms|ReadBlockOpAvgTime|userId, clusterId, and role|Average|
|ReadBlockOpNumOps|N/A|ReadBlockOpNumOps|userId, clusterId, and role|Average|
|ReceivedBytes|N/A|ReceivedBytes|userId, clusterId, and role|Average|
|ReplaceBlockOpAvgTime|ms|ReplaceBlockOpAvgTime|userId, clusterId, and role|Average|
|ReplaceBlockOpNumOps|N/A|ReplaceBlockOpNumOps|userId, clusterId, and role|Average|
|RequestHandlerAvgIdlePercent|N/A|RequestHandlerAvgIdlePercent|userId, clusterId, and role|Average|
|RequestQueueUsagePercent|N/A|RequestQueueUsagePercent|userId, clusterId, and role|Average|
|ReservedContainers|N/A|ReservedContainers|userId, clusterId, and role|Average|
|ResourceManagerActive|N/A|ResourceManagerActive|userId, clusterId, and role|Average|
|ResourceManagerAdminPortOpen|N/A|ResourceManagerAdminPortOpen|userId, clusterId, and role|Average|
|ResourceManagerPortOpen|N/A|ResourceManagerPortOpen|userId, clusterId, and role|Average|
|ResourceManagerResourcetrackerPortOpen|N/A|ResourceManagerResourcetrackerPortOpen|userId, clusterId, and role|Average|
|ResourceManagerSchedulerPortOpen|N/A|ResourceManagerSchedulerPortOpen|userId, clusterId, and role|Average|
|ResourceManagerWebappPortOpen|N/A|ResourceManagerWebappPortOpen|userId, clusterId, and role|Average|
|RevisedNumLostNMS|N/A|RevisedNumLostNMS|userId, clusterId, and role|Average|
|ScheduledReplicationBlocks|N/A|ScheduledReplicationBlocks|userId, clusterId, and role|Average|
|SendBytes|N/A|SendBytes|userId, clusterId, and role|Average|
|SparkHistoryServerUiPortOpen|N/A|SparkHistoryServerUiPortOpen|userId, clusterId, and role|Average|
|StormNimbusThriftPortOpen|N/A|StormNimbusThriftPortOpen|userId, clusterId, and role|Average|
|StormUiPortOpen|N/A|StormUiPortOpen|userId, clusterId, and role|Average|
|ThreadsBlocked|N/A|ThreadsBlocked|userId, clusterId, and role|Average|
|ThreadsNew|N/A|ThreadsNew|userId, clusterId, and role|Average|
|ThreadsRunnable|N/A|ThreadsRunnable|userId, clusterId, and role|Average|
|ThreadsTerminated|N/A|ThreadsTerminated|userId, clusterId, and role|Average|
|ThreadsTimedWaiting|N/A|ThreadsTimedWaiting|userId, clusterId, and role|Average|
|ThreadsWainting|N/A|ThreadsWainting|userId, clusterId, and role|Average|
|ThriftServerInfoPortOpen|N/A|ThriftServerInfoPortOpen|userId, clusterId, and role|Average|
|ThriftServerJmxPortOpen|N/A|ThriftServerJmxPortOpen|userId, clusterId, and role|Average|
|ThriftServerPortOpen|N/A|ThriftServerPortOpen|userId, clusterId, and role|Average|
|TimelineSrverPortOpen|N/A|TimelineSrverPortOpen|userId, clusterId, and role|Average|
|TimelineServerWebappPortOpen|N/A|TimelineServerWebappPortOpen|userId, clusterId, and role|Average|
|TotalDFSUsedPercent|N/A|TotalDFSUsedPercent|userId, clusterId, and role|Average|
|TotalFiles|N/A|TotalFiles|userId, clusterId, and role|Average|
|TotalLoad|N/A|TotalLoad|userId, clusterId, and role|Average|
|UnderReplicatedBlocks|N/A|UnderReplicatedBlocks|userId, clusterId, and role|Average|
|VVPAppManagerPortOpen|count|VVPAppManagerPortOpen|userId, clusterId, and role|Average, Maximum, and Minimum|
|VVPGatewayPortOpen|count|VVPGatewayPortOpen|userId, clusterId, and role|Average, Maximum, and Minimum|
|VVPUiPortOpen|count|VVPUiPortOpen|userId, clusterId, and role|Average, Maximum, and Minimum|
|VolumeFailuers|N/A|VolumeFailuers|userId, clusterId, and role|Average|
|WriteBlockOpAvgTime|ms|WriteBlockOpAvgTime|userId, clusterId, and role|Average|
|WriteBlockOpNumOps|N/A|WriteBlockOpNumOps|userId, clusterId, and role|Average|
|YarnAppsFailed|N/A|YarnAppsFailed|userId, clusterId, and role|Average, Maximum, and Minimum|
|YarnRootActiveAppLications|N/A|YarnRootActiveAppLications|userId, clusterId, and role|Average, Maximum, and Minimum|
|YarnRootActiveUsers|N/A|YarnRootActiveUsers|userId, clusterId, and role|Average, Maximum, and Minimum|
|YarnRootAllocatedContainers|N/A|YarnRootAllocatedContainers|userId, clusterId, and role|Average, Maximum, and Minimum|
|YarnRootAllocatedMB|N/A|YarnRootAllocatedMB|userId, clusterId, and role|Average, Maximum, and Minimum|
|YarnRootAllocatedVCores|N/A|YarnRootAllocatedVCores|userId, clusterId, and role|Average, Maximum, and Minimum|
|YarnRootAppsCompleted|N/A|YarnRootAppsCompleted|userId, clusterId, and role|Average, Maximum, and Minimum|
|YarnRootAppsKilled|N/A|YarnRootAppsKilled|userId, clusterId, and role|Average, Maximum, and Minimum|
|YarnRootAppsPending|N/A|YarnRootAppsPending|userId, clusterId, and role|Average, Maximum, and Minimum|
|YarnRootAppsRunning|N/A|YarnRootAppsRunning|userId, clusterId, and role|Average, Maximum, and Minimum|
|YarnRootAppsSubmitted|N/A|YarnRootAppsSubmitted|userId, clusterId, and role|Average, Maximum, and Minimum|
|YarnRootAvailableMB|N/A|YarnRootAvailableMB|userId, clusterId, and role|Average, Maximum, and Minimum|
|YarnRootAvailableVCores|N/A|YarnRootAvailableVCores|userId, clusterId, and role|Average, Maximum, and Minimum|
|YarnRootPendingContainers|N/A|YarnRootPendingContainers|userId, clusterId, and role|Average, Maximum, and Minimum|
|YarnRootPendingMB|N/A|YarnRootPendingMB|userId, clusterId, and role|Average, Maximum, and Minimum|
|YarnRootPendingVCores|N/A|YarnRootPendingVCores|userId, clusterId, and role|Average, Maximum, and Minimum|
|YarnRootReservedContainers|N/A|YarnRootReservedContainers|userId, clusterId, and role|Average, Maximum, and Minimum|
|YarnRootReservedMB|N/A|YarnRootReservedMB|userId, clusterId, and role|Average, Maximum, and Minimum|
|YarnRootReservedVCores|N/A|YarnRootReservedVCores|userId, clusterId, and role|Average, Maximum, and Minimum|
|ZKAvgLatency|N/A|ZKAvgLatency|userId, clusterId, and role|Average|
|ZKClientPortOpen|N/A|ZKClientPortOpen|userId, clusterId, and role|Average|
|ZKFCPortOpen|N/A|ZKFCPortOpen|userId, clusterId, and role|Average|
|ZKLsLeader|N/A|ZKLsLeader|userId, clusterId, and role|Average|
|ZKLeaderPortOpen|N/A|ZKLeaderPortOpen|userId, clusterId, and role|Average|
|ZKPeerPortOpen|N/A|ZKPeerPortOpen|userId, clusterId, and role|Average|
|ZeppelinPortOpen|N/A|ZeppelinPortOpen|userId, clusterId, and role|Average|
|ZkMaxFileDescriptorCount|N/A|ZkMaxFileDescriptorCount|userId, clusterId, and role|Average|
|ZkMaxLatency|N/A|ZkMaxLatency|userId, clusterId, and role|Average|
|ZKMinLatency|N/A|ZKMinLatency|userId, clusterId, and role|Average|
|ZkNumAliveConnections|N/A|ZkNumAliveConnections|userId, clusterId, and role|Average|
|ZkOpenFileFescriptorCount|N/A|ZkOpenFileFescriptorCount|userId, clusterId, and role|Average|
|ZkOutStandingRequests|N/A|ZkOutStandingRequests|userId, clusterId, and role|Average|
|ZkPacketsReceived|N/A|ZkPacketsReceived|userId, clusterId, and role|Average|
|ZkPackersSent|N/A|ZkPackersSent|userId, clusterId, and role|Average|
|ZkWatchCount|N/A|ZkWatchCount|userId, clusterId, and role|Average|
|ZkZnodeCount|N/A|ZkZnodeCount|userId, clusterId, and role|Average|
|ZooKeeperAuthFailuresPerSec|N/A|ZooKeeperAuthFailuresPerSec|userId, clusterId, and role|Average|
|ZookeeperDisconnectsPerSec|N/A|ZookeeperDisconnectsPerSec|userId, clusterId, and role|Average|
|ZookeeperExpiresPerSec|N/A|ZookeeperExpiresPerSec|userId, clusterId, and role|Average|
|ZookeeperReadOnlyConnectsPerSec|N/A|ZookeeperReadOnlyConnectsPerSec|userId, clusterId, and role|Average|
|ZookeeperSaslAuthenticationsPerSec|N/A|ZookeeperSaslAuthenticationsPerSec|userId, clusterId, and role|Average|
|ZookeeperSyncConnectsPerSec|N/A|ZookeeperSyncConnectsPerSec|userId, clusterId, and role|Average|
|Inbound Bandwidth Rate|bit/s|bytes\_in|userId, clusterId, and role|Average|
|Outbound Bandwidth Rate|bit/s|byte\_out|userId, clusterId, and role|Average|
|Enable CPU Idle Rate|N/A|cpu\_aidle|userId, clusterId, and role|Average|
|CPU Idle Rate|%|cpu\_idle|userId, clusterId, and role|Average|
|CPU Hard Interrupt Time Consuming ratio|N/A|cpu\_intr|userId, clusterId, and role|Average|
|CPU\_NICE Utilization Rate|N/A|cpu\_nice|userId, clusterId, and role|Average|
|CPU Soft Interrupt Time Consuming ratio|N/A|cpu\_sintr|userId, clusterId, and role|Average|
|System State CPU Usage|%|cpu\_system|userId, clusterId, and role|Average|
|User CPU Usage|%|cpu\_user|userId, clusterId, and role|Average|
|CPU I/O Idle Rate|N/A|cpu\_wio|userId, clusterId, and role|Average|
|Free Disk Size|byte|disk\_free|userId, clusterId, and role|Average|
|Total Disk Size|byte|disk\_total|userId, clusterId, and role|Average|
|Average Load in 15 minutes|N/A|load\_fifteen|userId, clusterId, and role|Average|
|Average Load in 5 minutes|N/A|load\_five|userId, clusterId, and role|Average|
|Average Load in 1 minute|N/A|lod\_one|userId, clusterId, and role|Average|
|BUFFER Memory Size|N/A|mem\_buffers|userId, clusterId, and role|Average|
|CACHE Memory Size|N/A|mem\_cached|userId, clusterId, and role|Average|
|Free Memory Size|byte|mem\_free|userId, clusterId, and role|Average|
|SHARE Memory Size|N/A|mem\_shared|userId, clusterId, and role|Average|
|Total Memory Size|byte|mem\_total|userId, clusterId, and role|Average|
|mem\_used\_percent|N/A|mem\_userd\_percent|userId, clusterId, and role|Average|
|Maximum Usage of Disk Partitions|N/A|part\_max\_used|userId, clusterId, and role|Average|
|Inbound Data Package Rate|count/s|pkts\_in|userId, clusterId, and role|Average|
|Outbound Data Package Rate|count/s|pkts\_out|userId, clusterId, and role|Average|
|Outbound Data Package Rate|count|pkts\_run|userId, clusterId, and role|Average|
|Total Process Number|count|proc\_total|userId, clusterId, and role|Average|
|Blocked Process Number|count|procs\_blocked|userId, clusterId, and role|Average|
|Created Process/ Process Number|count|procs\_created|userId, clusterId, and role|Average|
|Idle Swap Size|N/A|swap\_free|userId, clusterId, and role|Average|
|Swap Total|N/A|swap\_total|userId, clusterId, and role|Average|
|ALINKServerPortOpen|count|ALINKServerPortOpen|userId, clusterId, role, and instanceId|Average, Maximum, and Minimum|
|ALINKNginxPortOpen|count|ALINKNginxPortOpen|userId, clusterId, role, and instanceId|Average, Maximum, and Minimum|
|YarnRootContainerPendingRatio|1|YarnRootContainerPendingRatio|userId, clusterId, role, and instanceId|Average, Maximum, and Minimum|
|YarnRootMemoryAvailablePercentage|%|YarnRootMemoryAvailablePercentage|userId, clusterId, role, and instanceId|Average, Maximum, and Minimum|
|YarnRootVCoreAvailablePercentage|%|YarnRootVCoreAvailablePercentage|userId, clusterId, role, and instanceId|Average, Maximum, and Minimum|

