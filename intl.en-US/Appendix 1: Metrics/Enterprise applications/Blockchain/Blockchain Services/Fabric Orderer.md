# Blockchain Services/Fabric Orderer

This topic describes the metrics for the orderers of Blockchain as a Service.

-   Set the **Namespace** parameter to **acs\_baas**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|OrdererBroadcastBlockCounter|Count|OrdererBroadcastBlockCounter|userId, instanceId, id, and channelId|Sum|
|OrdererBroadcastTransactionCounter|Count|OrdererBroadcastTransactionCounter|userId, instanceId, id, and channelId|Sum|
|OrdererCaHealthzCounter|Count|OrdererCaHealthzCounter|userId, instanceId, and id|Sum|
|OrdererLedgerStorageSize|Byte|OrdererLedgerStorageSize|userId, instanceId, id, and channelId|Value|
|OrdererOrdererHealthzCounter|Count|OrdererOrdererHealthzCounter|userId, instanceId, and id|Sum|
|OrdererTotalStorageSize|Byte|OrdererTotalStorageSize|userId, instanceId, and id|Value|

