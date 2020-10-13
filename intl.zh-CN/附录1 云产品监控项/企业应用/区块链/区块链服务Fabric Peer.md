# 区块链服务Fabric Peer

通过本文您可以了解区块链服务Fabric Peer的监控项。

-   **Namespace**为**acs\_baas**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|PeerBlockCommitTime|ms|PeerBlockCommitTime|userId、instanceId、id、channelId|Sum|
|PeerBlockProcessingTime|ms|PeerBlockProcessingTime|userId、instanceId、id、channelId|Sum|
|PeerCaHealthzCounter|Count|PeerCaHealthzCounter|userId、instanceId、id|Sum|
|PeerEndorsementCounter|Count|PeerEndorsementCounter|userId、instanceId、id|Sum|
|PeerEndorsementSuccessfulCounter|Count|PeerEndorsementSuccessfulCounter|userId、instanceId、id|Sum|
|PeerLedgerStorageSize|Byte|PeerLedgerStorageSize|userId、instanceId、id、channelId|Value|
|PeerPeerHealthzCounter|Count|PeerPeerHealthzCounter|userId、instanceId、id|Sum|
|PeerRecvBlockCounter|Count|PeerRecvBlockCounter|userId、instanceId、id、channelId|Sum|
|PeerRecvTransactionCounter|Count|PeerRecvTransactionCounter|userId、instanceId、id、channelId|Sum|
|PeerRecvTransactionSuccessfulCounter|Count|PeerRecvTransactionSuccessfulCounter|userId、instanceId、id、channelId|Sum|
|PeerSendBlockCounter|Count|PeerSendBlockCounter|userId、instanceId、id、channelId|Sum|
|PeerStateStorageSize|Byte|PeerStateStorageSize|userId、instanceId、id|Value|
|PeerTotalStorageSize|Byte|PeerTotalStorageSize|userId、instanceId、id|Value|

