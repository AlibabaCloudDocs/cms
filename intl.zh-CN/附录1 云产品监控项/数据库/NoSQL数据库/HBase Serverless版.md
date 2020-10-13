# HBase Serverless版

通过本文您可以了解云数据库HBase Serverless版的监控项。

-   **Namespace**为**acs\_hbaseserverless**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|实例所占空间|Byte|Instance\_storage\_size|userId、instanceId|Sum|
|delete|ms|delete|userId、instanceId|Average|
|get|ms|get|userId、instanceId|Average|
|put|ms|put|userId、instanceId|Average|
|读CU|qps|read\_cu|userId、instanceId|Sum|
|scan|ms|scan|userId、instanceId|Average|
|写入CU数|qps|write\_cu|userId、instanceId|Sum|

