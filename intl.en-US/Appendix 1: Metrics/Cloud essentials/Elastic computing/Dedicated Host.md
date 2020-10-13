# Dedicated Host

This topic describes the metrics for Dedicated Host \(DDH\).

-   Set the **Namespace** parameter to **acs\_ddh**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|UserCpuUtilization|%|UserCpuUtilization|userId and DedicatedHostId|Value|
|UserDiskReadBPS|byte/s|UserDiskReadBPS|userId and DedicatedHostId|Value|
|UserDiskReadIOPS|count/s|UserDiskReadIOPS|userId and DedicatedHostId|Value|
|UserDiskWriteBPS|byte/s|UserDiskWriteBPS|userId and DedicatedHostId|Value|
|UserDiskWriteIOPS|count/s|UserDiskWriteIOPS|userId and DedicatedHostId|Value|
|UserNetworkRxBandwidth|bit/s|UserNetworkRxBandwidth|userId and DedicatedHostId|Value|
|UserNetworkRxPPS|packet/s|UserNetworkRxPPS|userId and DedicatedHostId|Value|
|UserNetworkTxBandwidth|bit/s|UserNetworkTxBandwidth|userId and DedicatedHostId|Value|
|UserNetworkTxPPS|packet/s|UserNetworkTxPPS|userId and DedicatedHostId|Value|

