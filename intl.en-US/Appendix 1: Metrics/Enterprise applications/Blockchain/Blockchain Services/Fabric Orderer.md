# Blockchain Services/Fabric Orderer

This topic describes the metrics of the orderers of Blockchain as a Service.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_baas**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|AllOrdererTotalStorageSize|Byte|AllOrdererTotalStorageSize|userId and instanceId|Sum|
|OrdererBroadcastBlockCounter|Count|OrdererBroadcastBlockCounter|userId, instanceId, id, and channelId|Sum|
|OrdererBroadcastTransactionCounter|Count|OrdererBroadcastTransactionCounter|userId, instanceId, id, and channelId|Sum|
|OrdererCaHealthzCounter|Count|OrdererCaHealthzCounter|userId, instanceId, and id|Sum|
|OrdererLedgerStorageSize|Byte|OrdererLedgerStorageSize|userId, instanceId, id, and channelId|Value|
|OrdererOrdererHealthzCounter|Count|OrdererOrdererHealthzCounter|userId, instanceId, and id|Sum|
|OrdererSLBActiveConnection|Count|OrdererSLBActiveConnection|userId, instanceId, port, and protocol|Average|
|OrdererSLBTrafficRX|Byte|OrdererSLBTrafficRX|userId, instanceId, port, and protocol|Average|
|OrdererSLBTrafficTX|Byte|OrdererSLBTrafficTX|userId, instanceId, port, and protocol|Average|
|OrdererTotalStorageSize|Byte|OrdererTotalStorageSize|userId, instanceId, and id|Value|

