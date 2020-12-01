# PrivateLink-Endpoint

This topic describes the metrics of the endpoint of the Private Network Connection.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_privatelink**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

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
|Endpoint Zone Inbound Bandwidth|bit/s|VpcEndpointZoneInBps|userId, instanceId, and zoneId|Average|
|Endpoint Zone Inbound Bandwidth Drop|bit/s|VpcEndpointZoneInDropBps|userId, instanceId, and zoneId|Average|
|Endpoint Zone Inbound Packet Drop|packet/s|VpcEndpointZoneInDropPps|userId, instanceId, and zoneId|Average|
|Endpoint Zone Inbound Packet|packet/s|VpcEndpointZoneInPps|userId, instanceId, and zoneId|Average|
|Endpoint Zone Outbound Bandwidth|bit/s|VpcEndpointZoneOutBps|userId, instanceId, and zoneId|Average|
|Endpoint Zone Outbound Bandwidth Drop|bit/s|VpcEndpointZoneOutDropBps|userId, instanceId, and zoneId|Average|
|Endpoint Zone Outbound Packet Drop|packet/s|VpcEndpointZoneOutDropPps|userId, instanceId, and zoneId|Average|
|Endpoint Zone Outbound Packet|packet/s|VpcEndpointZoneOutPps|userId, instanceId, and zoneId|Average|

