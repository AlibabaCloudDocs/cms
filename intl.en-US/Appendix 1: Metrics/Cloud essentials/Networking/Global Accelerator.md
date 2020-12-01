# Global Accelerator

This topic describes the metrics of Global Accelerator \(GA\).

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_global\_acceleration**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|GaIpInBps|bits/s|GaIpInBps|userId, instanceId, and regionId|Average|
|GaIpInPps|pps|GaIpInPps|userId, instanceId, and regionId|Average|
|GaIpOutBps|bits/s|GaIpOutBps|userId, instanceId, and regionId|Average|
|GaIpOutPps|pps|GaIpOutPps|userId, instanceId, and regionId|Average|
|GaIpActiveConnectionCount|Count|GaIpActiveConnectionCount|userId, instanceId, and regionId|Average|
|GaIpInDropPps|pps|GaIpInDropPps|userId, instanceId, and regionId|Average|
|GaIpOutDropPps|pps|GaIpOutDropPps|userId, instanceId, and regionId|Average|
|GaNetworkProbeAcceleratorDrop|pps|GaNetworkProbeAcceleratorDrop|userId, instanceId, regionId, endpointGroupId, and targetIp|Average|
|GaNetworkProbeAcceleratorLatency|s|GaNetworkProbeAcceleratorLatency|userId, instanceId, regionId, endpointGroupId, and targetIp|Average|
|GaNetworkProbeInternetDrop|pps|GaNetworkProbeInternetDrop|userId, instanceId, regionId, endpointGroupId, and targetIp|Average|
|GaNetworkProbeInternetLatency|s|GaNetworkProbeInternetLatency|userId, instanceId, regionId, endpointGroupId, and targetIp|Average|

