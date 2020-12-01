# SLB

This topic describes the metrics of Server Load Balancer \(SLB\).

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_slb\_dashboard**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Number of Active Port Connections|Count|ActiveConnection|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|Number of Discarded Port Connections|CountSecond|DropConnection|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|Number of Discarded Inbound Data Packets by Port|CountSecond|DropPacketRX|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|Number of Discarded Outbound Data Packets by Port|CountSecond|DropPacketTX|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|Number of Discarded Inbound Bandwidth by Port|bit/s|DropTrafficRX|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|Number of Discarded Outbound Bandwidth by Port|bit/s|DropTrafficTX|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|Number of Backend Healthy ECS Instances by Port|Count|HeathyServerCount|userId, instanceId, port, and vip|Maximum, Minimum, and Average|
|Number of Inactive Port Connections|Count|InactiveConnection|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|Number of Active Instance Connections|CountSecond|InstanceActiveConnection|userId and instanceId|Maximum, Minimum, and Average|
|Number of Discarded Instance Connections|CountSecond|InstanceDropConnection|userId and instanceId|Maximum, Minimum, and Average|
|Number of Discarded Inbound Data Packets by Instance|CountSecond|InstanceDropPacketRX|userId and instanceId|Maximum, Minimum, and Average|
|Number of Discarded Outbound Data Packets by Instance|CountSecond|InstanceDropPacketTX|userId and instanceId|Maximum, Minimum, and Average|
|Discarded Inbound Bandwidth by Instance|bit/s|InstanceDropTrafficRX|userId and instanceId|Maximum, Minimum, and Average|
|Discarded Outbound Bandwidth by Instance|bit/s|InstanceDropTrafficTX|userId and instanceId|Maximum, Minimum, and Average|
|Number of Inactive Instance Connections|CountSecond|InstanceInactiveConnection|userId and instanceId|Maximum, Minimum, and Average|
|Number of Concurrent Instance Connections|CountSecond|InstanceMaxConnection|userId and instanceId|Maximum, Minimum, and Average|
|Instance Max Connection Utilization|%|InstanceMaxConnectionUtilization|userId and instanceId|Maximum, Minimum, and Average|
|Number of New Instance Connections|CountSecond|InstanceNewConnection|userId and instanceId|Maximum, Minimum, and Average|
|InstanceNewConnectionUtilization|%|InstanceNewConnectionUtilization|userId and instanceId|Maximum, Minimum, and Average|
|Number of Inbound Data Packets by Instance|CountSecond|InstancePacketRX|userId and instanceId|Maximum, Minimum, and Average|
|Number of Outbound Data Packets by Instance|CountSecond|InstancePacketTX|userId and instanceId|Maximum, Minimum, and Average|
|Layer-7 Protocol Instance QPS|CountSecond|InstanceQps|userId and instanceId|Average|
|QPS Usage|%|InstanceQpsUtilization|userId and instanceId|Maximum, Minimum, and Average|
|Layer-7 Protocol Instance RT|ms|InstanceRt|userId and instanceId|Average|
|2XX Status Code of Layer-7 Protocol Instance|CountSecond|InstanceStatusCode2xx|userId and instanceId|Average|
|3XX Status Code of Layer-7 Protocol Instance|CountSecond|InstanceStatusCode3xx|userId and instanceId|Average|
|4XX Status Code of Layer-7 Protocol Instance|CountSecond|InstanceStatusCode4xx|userId and instanceId|Average|
|5XX Status Code of Layer-7 Protocol Instance|CountSecond|InstanceStatusCode5xx|userId and instanceId|Average|
|Other Status Codes of Layer-7 Protocol Instance|CountSecond|InstanceStatusCodeOther|userId and instanceId|Average|
|Number of Inbound Bandwidth by Instance|bit/s|InstanceTrafficRX|userId and instanceId|Maximum, Minimum, and Average|
|Number of Outbound Bandwidth by Instance|bit/s|InstanceTrafficTX|userId and instanceId|Maximum, Minimum, and Average|
|4xx Status Code of Upstream on Layer-7 Protocol Instance|CountSecond|InstanceUpstreamCode4xx|userId and instanceId|Average|
|5xx Status Code of Upstream on Layer-7 Protocol Instance|CountSecond|InstanceUpstreamCode5xx|userId and instanceId|Average|
|UpstreamRT on Layer-7 Protocol Instance|ms|InstanceUpstreamRt|userId and instanceId|Average|
|Number of Concurrent Port Connections|CountSecond|MaxConnection|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|Number of New Port Connections|Count|NewConnection|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|Number of Inbound Data Packets by Port|CountSecond|PacketRX|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|Number of Outbound Data Packets by Port|CountSecond|PacketTX|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|Layer-7 Protocol Port QPS|CountSecond|Qps|userId, instanceId, port, and protocol|Average|
|Layer-7 Protocol Port RT|ms|Rt|userId, instanceId, port, and protocol|Average|
|2XX Status Code of Layer-7 Protocol Port|CountSecond|StatusCode2xx|userId, instanceId, port, and protocol|Average|
|3XX Status Code of Layer-7 Protocol Port|CountSecond|StatusCode3xx|userId, instanceId, port, and protocol|Average|
|4XX Status Code of Layer-7 Protocol Port|CountSecond|StatusCode4xx|userId, instanceId, port, and protocol|Average|
|5XX Status Code of Layer-7 Protocol Port|CountSecond|StatusCode5xx|userId, instanceId, port, and protocol|Average|
|Other Status Codes of Layer-7 Protocol Port|CountSecond|StatusCodeOther|userId, instanceId, port, and protocol|Average|
|Port Inbound Bandwidth|bit/s|TrafficRXNew|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|Port Outbound Bandwidth|bit/s|TrafficTXNew|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|Number of Backend Unhealthy ECS Instances by Port|Count|UnhealthyServerCount|userId, instanceId, port, and vip|Maximum, Minimum, and Average|
|4xx Status Code of Upstream on Layer-7 Protocol Port|CountSecond|UpstreamCode4xx|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|5xx Status Code of Upstream on Layer-7 Protocol Port|CountSecond|UpstreamCode5xx|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|Layer-7 Protocol Instance UpstreamRt|ms|UpstreamRt|userId, instanceId, port, and protocol|Average|
|InternetOutRatePercent|%|InstanceTrafficTXUtilization|userId and instanceId|Maximum, Minimum, and Average|

