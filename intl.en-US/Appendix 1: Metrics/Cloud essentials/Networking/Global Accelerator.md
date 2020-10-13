# Global Accelerator

This topic describes the metrics for Global Accelerator \(GA\).

-   Set the **Namespace** parameter to **acs\_global\_acceleration**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|GaIpInBps|bit/s|GaIpInBps|userId, instanceId, and regionId|Average|
|GaIpInPps|packet/s|GaIpInPps|userId, instanceId, and regionId|Average|
|GaIpOutBps|bit/s|GaIpOutBps|userId, instanceId, and regionId|Average|
|GaIpOutPps|packet/s|GaIpOutPps|userId, instanceId, and regionId|Average|
|GaIpActiveConnectionCount|count|GaIpActiveConnectionCount|userId, instanceId, and regionId|Average|
|GaIpInDropPps|packet/s|GaIpInDropPps|userId, instanceId, and regionId|Average|
|GaIpOutDropPps|packet/s|GaIpOutDropPps|userId, instanceId, and regionId|Average|

