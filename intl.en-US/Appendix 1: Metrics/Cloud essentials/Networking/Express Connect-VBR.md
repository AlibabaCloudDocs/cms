# Express Connect-VBR

This topic describes the metrics of Express Connect-VBR.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_physical\_connection**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|BytesOutFromVpcToIDC|Bytes|BytesOutFromVpcToIDC|userId and instanceId|Value|
|PkgsDropInFromIDCToVpc|pps|PkgsDropInFromIDCToVpc|userId and instanceId|Value|
|PkgsDropOutFromVpcToIDC|pps|PkgsDropOutFromVpcToIDC|userId and instanceId|Value|
|PkgsInFromIDCToVpc|pps|PkgsInFromIDCToVpc|userId and instanceId|Value|
|PkgsOutFromVpcToIDC|pps|PkgsOutFromVpcToIDC|userId and instanceId|Value|
|RateInFromIDCToVpc|bps|RateInFromIDCToVpc|userId and instanceId|Value|
|RateOutFromVpcToIDC|bps|RateOutFromVpcToIDC|userId and instanceId|Value|
|VbrHealthyCheckLatency|μs|VbrHealthyCheckLatency|userId and instanceId|Value|
|VbrHealthyCheckLossRate|%|VbrHealthyCheckLossRate|userId and instanceId|Value|

