# HBase Serverless版

通过本文您可以了解云数据库HBase Serverless版的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_hbaseserverless**。
-   **Period**默认为60秒，也可以为60的整数倍。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|实例所占空间|Bytes|Instance\_storage\_size|userId、instanceId|Sum|
|Delete|ms|delete|userId、instanceId|Average|
|Get|ms|get|userId、instanceId|Average|
|Put|ms|put|userId、instanceId|Average|
|读CU|request per min|read\_cu|userId、instanceId|Sum|
|Scan|ms|scan|userId、instanceId|Average|
|写入CU数|request per min|write\_cu|userId、instanceId|Sum|

