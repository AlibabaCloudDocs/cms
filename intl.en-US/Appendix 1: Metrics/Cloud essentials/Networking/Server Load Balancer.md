# Server Load Balancer

This topic describes the metrics for Server Load Balancer \(SLB\).

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for ApsaraDB for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_slb\_dashboard**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Number of Active Port Connections|count|ActiveConnection|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|Number of Discarded Port Connections|count/s|DropConnection|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|Number of Discarded Inbound Data Packets by Port|count/s|DropPacketRX|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|Number of Discarded Outbound Data Packets by Port|count/s|DropPacketTX|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|Number of Discarded Inbound Bandwidth by Port|bit/s|DropTrafficRX|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|Number of Discarded Outbound Bandwidth by Port|bit/s|DropTrafficTX|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|Number of Backend Healthy ECS Instances by Port|count|HeathyServerCount|userId, instanceId, port, and vip|Maximum, Minimum, and Average|
|Number of Inactive Port Connections|count|InactiveConnection|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|Number of Active Instance Connections|count/s|InstanceActiveConnection|userId and instanceId|Maximum, Minimum, and Average|
|Number of Discarded Instance Connections|count/s|InstanceDropConnection|userId and instanceId|Maximum, Minimum, and Average|
|Number of Discarded Inbound Data Packets by Instance|count/s|InstanceDropPacketRX|userId and instanceId|Maximum, Minimum, and Average|
|Number of Discarded Outbound Data Packets by Instance|count/s|InstanceDropPacketTX|userId and instanceId|Maximum, Minimum, and Average|
|Discarded Inbound Bandwidth by Instance|bit/s|InstanceDropTrafficRX|userId and instanceId|Maximum, Minimum, and Average|
|Discarded Outbound Bandwidth by Instance|bit/s|InstanceDropTrafficTX|userId and instanceId|Maximum, Minimum, and Average|
|Number of Inactive Instance Connections|count/s|InstanceInactiveConnection|userId and instanceId|Maximum, Minimum, and Average|
|Number of Concurrent Instance Connections|count/s|InstanceMaxConnection|userId and instanceId|Maximum, Minimum, and Average|
|Instance Max Connection Utilization|%|InstanceMaxConnectionUtilization|userId and instanceId|Maximum, Minimum, and Average|
|Number of New Instance Connections|count/s|InstanceNewConnection|userId and instanceId|Maximum, Minimum, and Average|
|InstanceNewConnectionUtilization|%|InstanceNewConnectionUtilization|userId and instanceId|Maximum, Minimum, and Average|
|Number of Inbound Data Packets by Instance|count/s|InstancePacketRX|userId and instanceId|Maximum, Minimum, and Average|
|Number of Outbound Data Packets by Instance|count/s|InstancePacketTX|userId and instanceId|Maximum, Minimum, and Average|
|Layer-7 Protocol Instance QPS|count/s|InstanceQps|userId and instanceId|Average|
|InstanceQpsUtilization|%|InstanceQpsUtilization|userId and instanceId|Maximum, Minimum, and Average|
|Layer-7 Protocol Instance RT|ms|InstanceRt|userId and instanceId|Average|
|2XX Status Code of Layer-7 Protocol Instance|count/s|InstanceStatusCode2xx|userId and instanceId|Average|
|3XX Status Code of Layer-7 Protocol Instance|count/s|InstanceStatusCode3xx|userId and instanceId|Average|
|4XX Status Code of Layer-7 Protocol Instance|count/s|InstanceStatusCode4xx|userId and instanceId|Average|
|5XX Status Code of Layer-7 Protocol Instance|count/s|InstanceStatusCode5xx|userId and instanceId|Average|
|Other Status Codes of Layer-7 Protocol Instance|count/s|InstanceStatusCodeOther|userId and instanceId|Average|
|Number of Inbound Bandwidth by Instance|bit/s|InstanceTrafficRX|userId and instanceId|Maximum, Minimum, and Average|
|Number of Outbound Bandwidth by Instance|bit/s|InstanceTrafficTX|userId and instanceId|Maximum, Minimum, and Average|
|4xx Status Code of Upstream on Layer-7 Protocol Instance|count/s|InstanceUpstreamCode4xx|userId and instanceId|Average|
|5xx Status Code of Upstream on Layer-7 Protocol Instance|count/s|InstanceUpstreamCode5xx|userId and instanceId|Average|
|UpstreamRT on Layer-7 Protocol Instance|ms|InstanceUpstreamRt|userId and instanceId|Average|
|Number of Concurrent Port Connections|count/s|MaxConnection|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|Number of New Port Connections|count|NewConnection|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|Number of Inbound Data Packets by Port|count/s|PacketRX|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|Number of Outbound Data Packets by Port|count/s|PacketTX|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|Layer-7 Protocol Port QPS|count/s|Qps|userId, instanceId, port, and protocol|Average|
|Layer-7 Protocol Port RT|ms|Rt|userId, instanceId, port, and protocol|Average|
|2XX Status Code of Layer-7 Protocol Port|count/s|StatusCode2xx|userId, instanceId, port, and protocol|Average|
|3XX Status Code of Layer-7 Protocol Port|count/s|StatusCode3xx|userId, instanceId, port, and protocol|Average|
|4XX Status Code of Layer-7 Protocol Port|count/s|StatusCode4xx|userId, instanceId, port, and protocol|Average|
|5XX Status Code of Layer-7 Protocol Port|count/s|StatusCode5xx|userId, instanceId, port, and protocol|Average|
|Other Status Codes of Layer-7 Protocol Port|count/s|StatusCodeOther|userId, instanceId, port, and protocol|Average|
|Port Inbound Bandwidth|bit/s|TrafficRXNew|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|Port Outbound Bandwidth|bit/s|TrafficTXNew|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|Number of Backend Unhealthy ECS Instances by Port|count|UnhealthyServerCount|userId, instanceId, port, and vip|Maximum, Minimum, and Average|
|4xx Status Code of Upstream on Layer-7 Protocol Port|count/s|UpstreamCode4xx|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|5xx Status Code of Upstream on Layer-7 Protocol Port|count/s|UpstreamCode5xx|userId, instanceId, port, and protocol|Maximum, Minimum, and Average|
|Layer-7 Protocol Instance UpstreamRt|ms|UpstreamRt|userId, instanceId, port, and protocol|Average|

