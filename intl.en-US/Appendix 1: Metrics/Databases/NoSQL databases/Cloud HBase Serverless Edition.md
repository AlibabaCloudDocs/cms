# Cloud HBase Serverless Edition

This topic describes the metrics of ApsaraDB for HBase Serverless Edition.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_hbaseserverless**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Instance storage size|Bytes|Instance\_storage\_size|userId and instanceId|Sum|
|Delete|ms|delete|userId and instanceId|Average|
|Get|ms|get|userId and instanceId|Average|
|Put|ms|put|userId and instanceId|Average|
|read cu qps|request per min|read\_cu|userId and instanceId|Sum|
|Scan|ms|scan|userId and instanceId|Average|
|write cu QPS|request per min|write\_cu|userId and instanceId|Sum|

