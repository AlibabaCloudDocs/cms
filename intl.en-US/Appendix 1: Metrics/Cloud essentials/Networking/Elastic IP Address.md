# Elastic IP Address

This topic describes the metrics of Anycast Elastic IP address \(EIP\).

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** to **acs\_anycast\_eip**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|InboundBandwidth|bits/s|InboundBandwidth|userId, instanceId, and regionNo|Value|
|InboundBandwidthUsage|Value|InboundBandwidthUsage|userId, instanceId, and regionNo|Value|
|InboundPacketRate|Packets/Second|InboundPacketRate|userId, instanceId, and regionNo|Value|
|InboundRatelimitDropBandwidth|bits/s|InboundRatelimitDropBandwidth|userId, instanceId, and regionNo|Value|
|InboundRatelimitDropSpeed|Packets/Second|InboundRatelimitDropSpeed|userId, instanceId, and regionNo|Value|
|OutboundBandwidth|bits/s|OutboundBandwidth|userId, instanceId, and regionNo|Value|
|OutboundBandwidthUsage|Value|OutboundBandwidthUsage|userId, instanceId, and regionNo|Value|
|OutboundPacketRate|Packets/Second|OutboundPacketRate|userId, instanceId, and regionNo|Value|
|OutboundRatelimitDropBandwidth|bits/s|OutboundRatelimitDropBandwidth|userId, instanceId, and regionNo|Value|
|OutboundRatelimitDropSpeed|Packets/Second|OutboundRatelimitDropSpeed|userId, instanceId, and regionNo|Value|

