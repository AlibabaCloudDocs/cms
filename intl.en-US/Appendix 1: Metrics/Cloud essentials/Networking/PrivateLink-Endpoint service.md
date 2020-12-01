# PrivateLink-Endpoint service

This topic describes the metrics of the endpoint service of the Private Network Connection.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_privatelink**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Service Endpoint Zone Inbound Packet|packet/s|VpcEndpointServiceEndpointZoneInPps|userId, instanceId, endpointId, and zoneId|Average|
|Service Endpoint Zone Outbound Bandwidth|bit/s|VpcEndpointServiceEndpointZoneOutBps|userId, instanceId, endpointId, and zoneId|Average|
|Service Endpoint Zone Outbound Bandwidth Drop|bit/s|VpcEndpointServiceEndpointZoneOutDropBps|userId, instanceId, endpointId, and zoneId|Average|
|Service Endpoint Zone Outbound Packet Drop|packet/s|VpcEndpointServiceEndpointZoneOutDropPps|userId, instanceId, endpointId, and zoneId|Average|
|Service Endpoint Zone Outbound Packet|packet/s|VpcEndpointServiceEndpointZoneOutPps|userId, instanceId, endpointId, and zoneId|Average|
|Service Inbound Bandwidth|bit/s|VpcEndpointServiceInBps|userId and instanceId|Average|
|Service Inbound Bandwidth Drop|bit/s|VpcEndpointServiceInDropBps|userId and instanceId|Average|
|Service Outbound Bandwidth|bit/s|VpcEndpointServiceOutBps|userId and instanceId|Average|
|Service Outbound Bandwidth Drop|bit/s|VpcEndpointServiceOutDropBps|userId and instanceId|Average|
|Service Outbound Packet Drop|packet/s|VpcEndpointServiceOutDropPps|userId and instanceId|Average|
|Service Outbound Packet|packet/s|VpcEndpointServiceOutPps|userId and instanceId|Average|
|Service Resource Inbound Bandwidth|bit/s|VpcEndpointServiceResourceInBps|userId, instanceId, zoneId, and resourceId|Average|
|Service Resource Inbound Bandwidth Drop|bit/s|VpcEndpointServiceResourceInDropBps|userId, instanceId, zoneId, and resourceId|Average|
|Service Resource Inbound Packet Drop|packet/s|VpcEndpointServiceResourceInDropPps|userId, instanceId, zoneId, and resourceId|Average|
|Service Resource Inbound Packet|packet/s|VpcEndpointServiceResourceInPps|userId, instanceId, zoneId, and resourceId|Average|
|Service Resource Outbound Bandwidth|bit/s|VpcEndpointServiceResourceOutBps|userId, instanceId, zoneId, and resourceId|Average|
|Service Resource Outbound Bandwidth Drop|bit/s|VpcEndpointServiceResourceOutDropBps|userId, instanceId, zoneId, and resourceId|Average|
|Service Resource Outbound Packet Drop|packet/s|VpcEndpointServiceResourceOutDropPps|userId, instanceId, zoneId, and resourceId|Average|
|Service Resource Outbound Packet|packet/s|VpcEndpointServiceResourceOutPps|userId, instanceId, zoneId, and resourceId|Average|

