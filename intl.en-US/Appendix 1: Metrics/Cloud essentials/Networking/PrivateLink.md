# PrivateLink

This topic describes the metrics for PrivateLink.

-   Set the **Namespace** parameter to **acs\_privatelink**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|ENI Inbound Bandwidth|bit/s|EndpointENIInBps|userId, instanceId, and eniId|Average|
|ENI Inbound Bandwidth Drop|bit/s|EndpointENIInDropBps|userId, instanceId, and eniId|Average|
|ENI Inbound Packet Drop|packet/s|EndpointENIInDropPps|userId, instanceId, and eniId|Average|
|ENI Inbound Packet|packet/s|EndpointENIInPps|userId, instanceId, and eniId|Average|
|ENI Outbound Bandwidth|bit/s|EndpointENIOutBps|userId, instanceId, and eniId|Average|
|ENI Outbound Bandwidth Drop|bit/s|EndpointENIOutDropBps|userId, instanceId, and eniId|Average|
|ENI Outbound Packet Drop|packet/s|EndpointENIOutDropPps|userId, instanceId, and eniId|Average|
|ENI Outbound Packet|packet/s|EndpointENIOutPps|userId, instanceId, and eniId|Average|
|Endpoint Inbound Bandwidth|bit/s|EndpointInBps|userId and instanceId|Average|
|Endpoint Inbound Bandwidth Drop|bit/s|EndpointInDropBps|userId and instanceId|Average|
|Endpoint Inbound Packet Drop|packet/s|EndpointInDropPps|userId and instanceId|Average|
|Endpoint Inbound Packet|packet/s|EndpointInPps|userId and instanceId|Average|
|Endpoint Outbound Bandwidth|bit/s|EndpointOutBps|userId and instanceId|Average|
|Endpoint Outbound Bandwidth Drop|bit/s|EndpointOutDropBps|userId and instanceId|Average|
|Endpoint Outbound Packet Drop|packet/s|EndpointOutDropPps|userId and instanceId|Average|
|Endpoint Outbound Packet|packet/s|EndpointOutPps|userId and instanceId|Average|

