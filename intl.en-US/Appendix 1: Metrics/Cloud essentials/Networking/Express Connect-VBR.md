# Express Connect-VBR

This topic describes the metrics for Express Connect.

-   Set the **Namespace** parameter to **acs\_physical\_connection**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|PkgsDropInFromIDCToVpc|packet/s|PkgsDropInFromIDCToVpc|userId and instanceId|Value|
|PkgsDropOutFromVpcToIDC|packet/s|PkgsDropOutFromVpcToIDC|userId and instanceId|Value|
|PkgsInFromIDCToVpc|packet/s|PkgsInFromIDCToVpc|userId and instanceId|Value|
|PkgsOutFromVpcToIDC|packet/s|PkgsOutFromVpcToIDC|userId and instanceId|Value|
|RateInFromIDCToVpc|bit/s|RateInFromIDCToVpc|userId and instanceId|Value|
|RateOutFromVpcToIDC|bit/s|RateOutFromVpcToIDC|userId and instanceId|Value|
|VbrHealthyCheckLatency|μs|VbrHealthyCheckLatency|userId and instanceId|Value|
|VbrHealthyCheckLossRate|%|VbrHealthyCheckLossRate|userId and instanceId|Value|

