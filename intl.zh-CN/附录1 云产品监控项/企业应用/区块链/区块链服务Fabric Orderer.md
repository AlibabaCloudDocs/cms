# 区块链服务Fabric Orderer

通过本文您可以了解区块链服务Fabric Orderer的监控项。

-   **Namespace**为**acs\_baas**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|OrdererBroadcastBlockCounter|Count|OrdererBroadcastBlockCounter|userId、instanceId、id、channelId|Sum|
|OrdererBroadcastTransactionCounter|Count|OrdererBroadcastTransactionCounter|userId、instanceId、id、channelId|Sum|
|OrdererCaHealthzCounter|Count|OrdererCaHealthzCounter|userId、instanceId、id|Sum|
|OrdererLedgerStorageSize|Byte|OrdererLedgerStorageSize|userId、instanceId、id、channelId|Value|
|OrdererOrdererHealthzCounter|Count|OrdererOrdererHealthzCounter|userId、instanceId、id|Sum|
|OrdererTotalStorageSize|Byte|OrdererTotalStorageSize|userId、instanceId、id|Value|

