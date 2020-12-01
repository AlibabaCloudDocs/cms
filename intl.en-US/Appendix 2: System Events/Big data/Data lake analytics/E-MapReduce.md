# E-MapReduce

This topic describes the system events of E-MapReduce.

|Type|Event|Description|State|Level|
|----|-----|-----------|-----|-----|
|Flow|EMR-110401002|A workflow is completed.|Normal|Info|
|Flow|EMR-110401003|A workflow is submitted.|Normal|Info|
|Flow|EMR-110401004|A job is submitted.|Normal|Info|
|Flow|EMR-110401005|A workflow node is started.|Normal|Info|
|Flow|EMR-110401006|The status of a workflow node is checked.|Normal|Info|
|Flow|EMR-110401007|A workflow node is completed.|Normal|Info|
|Flow|EMR-110401008|A workflow node is stopped.|Normal|Info|
|Flow|EMR-110401009|A workflow node is canceled.|Normal|Info|
|Flow|EMR-110401010|A workflow is canceled.|Normal|Info|
|Flow|EMR-110401011|A workflow is restarted.|Normal|Info|
|Flow|EMR-110401012|A workflow is resumed.|Normal|Info|
|Flow|EMR-110401013|A workflow is paused.|Normal|Info|
|Flow|EMR-110401014|A workflow is stopped.|Normal|Info|
|Flow|EMR-110401015|A workflow node fails.|Normal|Info|
|Flow|EMR-110401016|A job fails.|Normal|Info|
|Flow|EMR-210401001|A workflow fails.|Normal|Info|
|Flow|EMR-210401003|The startup of a workflow node times out.|Normal|Info|
|Flow|EMR-210401004|The startup of a job times out.|Normal|Info|
|StatusNotification|StatusCheck|The status of a component is checked.|Failed|Warn|
|Maintenance|Maintenance:HDFS.DataNode.DataTransferPortUnAvailable|The data transmission port of a DataNode is unavailable.|Critical|Critical|
|Maintenance|Maintenance:HDFS.DataNode.ExitUnexpected|A DataNode unexpectedly exits.|Critical|Critical|
|Maintenance|Maintenance:HDFS.DataNode.IpcPortUnAvailable|The IPC port of a DataNode is unavailable.|Critical|Critical|
|Maintenance|Maintenance:HDFS.DataNode.OOM.UnableToCreateNewNativeThread|A DataNode cannot create a native thread due to an Out of Memory \(OOM\) exception that occurs in the DataNode.|Critical|Critical|
|Maintenance|Maintenance:HDFS.NameNode.IpcPortUnAvailable|The IPC port of the NameNode is unavailable.|Critical|Critical|
|Maintenance|Maintenance:HDFS.NameNode.LoadFsImageException|An exception occurs when the NameNode loads FsImage.|Critical|Critical|
|Maintenance|Maintenance:HDFS.NameNode.LowAvailableDiskSpaceAndInSafeMode|The NameNode is in safe mode due to insufficient disk space.|Critical|Critical|
|Maintenance|Maintenance:HDFS.NameNode.OOM|An OOM exception occurs in the NameNode.|Critical|Critical|
|Maintenance|Maintenance:HDFS.NameNode.ResourceLow|The NameNode does not have sufficient resources.|Critical|Critical|
|Maintenance|Maintenance:HDFS.NameNode.SyncJournalFailed|The NameNode fails to synchronize logs.|Critical|Critical|
|Maintenance|Maintenance:HDFS.ZKFC.ActiveStandbySwitchOccured|ZFKC triggers the NameNode failover.|Critical|Critical|
|Maintenance|Maintenance:HDFS.ZKFC.TransportLevelExceptionInMonitorHealth|A transport layer exception occurs when ZKFC monitors the health status of the NameNode.|Critical|Critical|
|Maintenance|Maintenance:HDFS.ZKFC.UnableToConnectToQuorum|ZKFC cannot connect to ZooKeeper Quorum.|Critical|Critical|
|Maintenance|Maintenance:HDFS.ZKFC.UnableToStartZKFC|ZKFC cannot be started.|Critical|Critical|
|Maintenance|Maintenance:HIVE.HiveMetaStore.DataBaseCommunicationLinkFailure|The communication link of the HiveMetaStore database fails.|Critical|Critical|
|Maintenance|Maintenance:HIVE.HiveMetaStore.DataBaseConnectionFailed|Failed to connect to the HiveMetaStore database.|Critical|Critical|
|Maintenance|Maintenance:HIVE.HiveMetaStore.DataBaseDiskQuotaUsedup|The HiveMetaStore database runs out of disk space.|Critical|Critical|
|Maintenance|Maintenance:HIVE.HiveMetaStore.JdbcCommunicationException|A JDC exception occurs in the HiveMetaStore.|Critical|Critical|
|Maintenance|Maintenance:HIVE.HiveMetaStore.MaxQuestionsExceeded|The number of queries for the HiveMetaStore exceeds the upper limit.|Critical|Critical|
|Maintenance|Maintenance:HIVE.HiveMetaStore.MaxUpdatesExceeded|The number of updates for the HiveMetaStore exceeds the upper limit.|Critical|Critical|
|Maintenance|Maintenance:HIVE.HiveMetaStore.MaxUserConnectionExceeded|The number of user connections for the HiveMetaStore exceeds the upper limit.|Critical|Critical|
|Maintenance|Maintenance:HIVE.HiveMetaStore.OomOccured|An OOM exception occurs in the HiveMetaStore.|Critical|Critical|
|Maintenance|Maintenance:HIVE.HiveMetaStore.ParseConfError|An error occurs when the HiveMetastore configuration file.|Critical|Critical|
|Maintenance|Maintenance:HIVE.HiveMetaStore.RequiredTableMissing|The required table of the HiveMetaStore is missing.|Critical|Critical|
|Maintenance|Maintenance:HIVE.HiveMetaStore.hiveServer2PortUnAvailable|The HIVE.HiveMetaStore.hiveServer2Port is unavailable.|Critical|Critical|
|Maintenance|Maintenance:HIVE.HiveServer2.ConnectToZkTimeout|The connection between the HiveServer2 and ZooKeeper times out.|Critical|Critical|
|Maintenance|Maintenance:HIVE.HiveServer2.ErrorParseConf|An error occurs when the HiveServer2 configuration is parsed.|Critical|Critical|
|Maintenance|Maintenance:HIVE.HiveServer2.ErrorStartingHiveServer|An error occurs when the HiveServer2 is stated.|Critical|Critical|
|Maintenance|Maintenance:HIVE.HiveServer2.FailedInitMetaStoreClient|The HiveServer2 fails to initialize the MetaStore client.|Critical|Critical|
|Maintenance|Maintenance:HIVE.HiveServer2.FailedToConnectToMetaStoreServer|The HiveServer2 fails to connect to the MetaStoreServer.|Critical|Critical|
|Maintenance|Maintenance:HIVE.HiveServer2.HiveServer2OOM|An OOM exception occurs in the HiveServer2.|Critical|Critical|
|Maintenance|Maintenance:HOST.OomFoundInVarLogMessage|An OOM exception occurs in the host/var/log/message directory.|Critical|Critical|
|Maintenance|Maintenance:SPARK.SparkHistory.OomOccured|An OOM occurs in the SparkHistory.|Critical|Critical|
|Maintenance|Maintenance:YARN.JobHistory.ExitUnExpectedly|The JobHistory service unexpectedly exits.|Critical|Critical|
|Maintenance|Maintenance:YARN.JobHistory.StartingError|An error occurs when the JobHistory service is stat.|Critical|Critical|
|Maintenance|Maintenance:YARN.NodeManager.DeadNodeDetected|One or more dead NodeManagers are detected.|Critical|Critical|
|Maintenance|Maintenance:YARN.NodeManager.OOM|An OOM exception occurs in a NodeManager.|Critical|Critical|
|Maintenance|Maintenance:YARN.NodeManager.StartingError|An error occurs when a NodeManager is started.|Critical|Critical|
|Maintenance|Maintenance:YARN.NodeManager.UnHealthyForDiskFailed|A NodeManager becomes unhealthy due to disk errors.|Critical|Critical|
|Maintenance|Maintenance:YARN.ResourceManager.ErrorInStarting|An error occurs when starting the ResourceManager.|Critical|Critical|
|Maintenance|Maintenance:YARN.ResourceManager.ErrorInTransitionToActiveMode|An error occurs when switching ResourceManager to the Active mode.|Critical|Critical|
|Maintenance|Maintenance:YARN.ResourceManager.ExitUnexpected|The ResourceManager unexpectedly exited.|Critical|Critical|
|Maintenance|Maintenance:YARN.ResourceManager.OOM|An OOM exception occurs in the ResourceManager.|Critical|Critical|
|Maintenance|Maintenance:YARN.ResourceManager.UnkownHostException|An UnkownHostException occurs in the ResourceManager.|Critical|Critical|
|Maintenance|Maintenance:YARN.ResourceManager.ZKRMStateStoreCannotConnectZK|In the YARN service, ZKRMStateStore cannot connect to ZooKeeper.|Critical|Critical|
|Maintenance|Maintenance:YARN.TimelineServer.ErrorInStarting|An error occurs when the TimelineServer.|Critical|Critical|
|Maintenance|Maintenance:YARN.TimelineServer.ExistUnexpectedly|The TimelineServer unexpectedly exits.|Critical|Critical|
|Maintenance|Maintenance:ZOOKEEPER.UnableToRunQuorumServer|The ZooKeeper cannot run QuorumServer.|Critical|Critical|
|Maintenance|Agent:Maintenance.EcmAgentTimeout|The EcmAgent remains disconnected for a long time.|Critical|Critical|
|Maintenance|Maintenance:ZOOKEEPER.LeaderPortUnAvailable|The LeaderPort of Zookeeper is unavailable.|Critical|Critical|
|Maintenance|Maintenance:ZOOKEEPER.ClientPortUnAvailable|The ClientPort of Zookeeper is unavailable.|Critical|Critical|
|Maintenance|Maintenance:YARN.NodeManager.UnHealthyNodesExist|One or more unhealthy nodes exist in YARN.|Critical|Critical|
|Maintenance|Maintenance:YARN.ResourceManager.ActiveStandbySwitch|A failover occurs in the ResourceManager.|Critical|Critical|
|Maintenance|Maintenance:YARN.ResourceManager.PortUnAvailable|The service port of the ResourceManager is unavailable.|Critical|Critical|
|Maintenance|Maintenance:STORM.Nimbus.ThriftPortUnAvailable|The STORM.Nimbus.ThriftPort is unavailable.|Critical|Critical|
|Exception|Agent:EcmAgentHeartbeatExpired|The heartbeat message of EcmAgent expires.|Critical|Critical|
|Maintenance|Maintenance:HDFS.DataNode.FailueVolumes|One or more damaged disks exist in the DataNode.|Critical|Critical|
|Maintenance|Maintenance:HDFS.JournalNode.RpcPortUnAvailable|The RPC port of the JournalNode is unavailable.|Critical|Critical|
|Maintenance|Maintenance:HDFS.NameNode.ActiveStandbySwitch|A failover occurs in the NameNode.|Critical|Critical|
|Maintenance|Maintenance:HDFS.NameNode.BlockCapacityNearUsedUp|The block capacity of the NameNode is running out.|Critical|Critical|
|Maintenance|Maintenance:HBASE.HMaster.IpcPortUnAvailable|The IPC port of the HBASE.HMaster is unavailable.|Critical|Critical|
|Maintenance|Maintenance:HBASE.HRegionServer.IpcPortUnAvailable|The IPC port of the HBASE.HRegionServer is unavailable.|Critical|Critical|
|Maintenance|Maintenance:HBASE.ThriftServer.ServicePortUnAvailable|The service port of the HBASE.ThriftServer is unavailable.|Critical|Critical|
|Maintenance|Maintenance:HUE.OozieAdminPortUnAvailable|The management port of Oozie is unavailable.|Critical|Critical|
|Maintenance|Maintenance:HUE.PortUnAvailable|The service port of HUE is unavailable.|Critical|Critical|
|Maintenance|Maintenance:HDFS.NameNode.InSafeMode|The NameNode remains in security mode for a long time.|Critical|Critical|
|Maintenance|Maintenance:HDFS.NameNode.MissingBlock|Data block is missing in HDFS.|Critical|Critical|
|Maintenance|Maintenance:HIVE.HiveMetaStore.PortUnAvailable|The port of the HIVE.HiveMetaStore is unavailable.|Critical|Critical|
|Scaling|Scaling:ScalingActivity:Failed|The auto scaling fails.|Normal|Critical|
|Scaling|Scaling:ScalingActivity:Timeout|The auto scaling times out.|Normal|Critical|
|Scaling|Scaling:ScalingActivity:Rejected|The auto scaling is rejected.|Normal|Critical|
|Maintenance|Maintenance:HOST.HighMemoryUsage|The memory usage is high.|Critical|Critical|
|Maintenance|Maintenance:HOST.LowDiskForMntDisk|The available space of /mnt/disk1 is too low.|Critical|Critical|
|Maintenance|Maintenance:HOST.LowRootfsDisk|The disk space available for the root file system is too low.|Critical|Critical|
|Maintenance|Maintenance:HIVE.HiveServer2.CannotConnectByAnyURIsProvided|Unable to connect to HiveServer2 by using the provided URIs.|Critical|Critical|

