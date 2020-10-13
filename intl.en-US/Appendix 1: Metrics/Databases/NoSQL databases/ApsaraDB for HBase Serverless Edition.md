# ApsaraDB for HBase Serverless Edition

This topic describes the metrics for ApsaraDB for HBase Serverless Edition.

-   Set the **Namespace** parameter to **acs\_hbaseserverless**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|Storage used by an instance|Byte|Instance\_storage\_size|userId and instanceId|Sum|
|delete|ms|delete|userId and instanceId|Average|
|get|ms|get|userId and instanceId|Average|
|put|ms|put|userId and instanceId|Average|
|Read capacity units \(CUs\)|qps|read\_cu|userId and instanceId|Sum|
|scan|ms|scan|userId and instanceId|Average|
|Write CUs|qps|write\_cu|userId and instanceId|Sum|

