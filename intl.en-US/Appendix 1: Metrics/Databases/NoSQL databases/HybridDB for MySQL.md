# HybridDB for MySQL

This topic describes the metrics for HybridDB for MySQL.

-   Set the **Namespace** parameter to **acs\_petadata**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Disk Usage|MB|DiskUsage|userId and instanceId|Average|
|Inbound Bandwidth|byte/s|InboundBandwidth|userId and instanceId|Average|
|Node CPU Usage|%|Node\_CPUUsage|userId, instanceId, schema, and nodeId|Average and Maximum|
|Node Disk Usage|MB|Node\_DiskUsage|userId, instanceId, schema, and nodeId|Average and Maximum|
|Node IOPS|count/s|Node\_IOPS|userId, instanceId, schema, and nodeId|Average and Maximum|
|Outbound Bandwidth|byte/s|OutBoundBandwidth|userId and instanceId|Average|
|QPS|count/s|QPS|userId and instanceId|Average, Maximum, and Minimum|

