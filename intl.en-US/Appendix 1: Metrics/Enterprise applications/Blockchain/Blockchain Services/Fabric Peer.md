# Blockchain Services/Fabric Peer

This topic describes the metrics for the peers of Blockchain as a Service.

-   Set the **Namespace** parameter to **acs\_baas**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|PeerBlockCommitTime|ms|PeerBlockCommitTime|userId, instanceId, id, and channelId|Sum|
|PeerBlockProcessingTime|ms|PeerBlockProcessingTime|userId, instanceId, id, and channelId|Sum|
|PeerCaHealthzCounter|Count|PeerCaHealthzCounter|userId, instanceId, and id|Sum|
|PeerEndorsementCounter|Count|PeerEndorsementCounter|userId, instanceId, and id|Sum|
|PeerEndorsementSuccessfulCounter|Count|PeerEndorsementSuccessfulCounter|userId, instanceId, and id|Sum|
|PeerLedgerStorageSize|Byte|PeerLedgerStorageSize|userId, instanceId, id, and channelId|Value|
|PeerPeerHealthzCounter|Count|PeerPeerHealthzCounter|userId, instanceId, and id|Sum|
|PeerRecvBlockCounter|Count|PeerRecvBlockCounter|userId, instanceId, id, and channelId|Sum|
|PeerRecvTransactionCounter|Count|PeerRecvTransactionCounter|userId, instanceId, id, and channelId|Sum|
|PeerRecvTransactionSuccessfulCounter|Count|PeerRecvTransactionSuccessfulCounter|userId, instanceId, id, and channelId|Sum|
|PeerSendBlockCounter|Count|PeerSendBlockCounter|userId, instanceId, id, and channelId|Sum|
|PeerStateStorageSize|Byte|PeerStateStorageSize|userId, instanceId, and id|Value|
|PeerTotalStorageSize|Byte|PeerTotalStorageSize|userId, instanceId, and id|Value|

