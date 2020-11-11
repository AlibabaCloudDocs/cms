# 区块链服务Fabric Orderer

通过本文您可以了解区块链服务Fabric Orderer的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_baas**。
-   **Period**默认为60秒，也可以为60的整数倍。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|AllOrdererTotalStorageSize|Byte|AllOrdererTotalStorageSize|userId、instanceId|Sum|
|OrdererBroadcastBlockCounter|Count|OrdererBroadcastBlockCounter|userId、instanceId、id、channelId|Sum|
|OrdererBroadcastTransactionCounter|Count|OrdererBroadcastTransactionCounter|userId、instanceId、id、channelId|Sum|
|OrdererCaHealthzCounter|Count|OrdererCaHealthzCounter|userId、instanceId、id|Sum|
|OrdererLedgerStorageSize|Byte|OrdererLedgerStorageSize|userId、instanceId、id、channelId|Value|
|OrdererOrdererHealthzCounter|Count|OrdererOrdererHealthzCounter|userId、instanceId、id|Sum|
|OrdererSLBActiveConnection|Count|OrdererSLBActiveConnection|userId、instanceId、port、protocol|Average|
|OrdererSLBTrafficRX|Byte|OrdererSLBTrafficRX|userId、instanceId、port、protocol|Average|
|OrdererSLBTrafficTX|Byte|OrdererSLBTrafficTX|userId、instanceId、port、protocol|Average|
|OrdererTotalStorageSize|Byte|OrdererTotalStorageSize|userId、instanceId、id|Value|

