# CDN

通过本文您可以了解CDN的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_cdn**。
-   **Period**默认为60秒，也可以为60的整数倍。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|499状态码个数|%|code\_count\_499|userId、instanceId|Average、Maximum、Minimum|
|499状态码比例|%|code\_ratio\_499|userId、instanceId|Average、Maximum、Minimum|
|用户维度状态码499个数|%|user\_code\_count\_499|userId|Average、Maximum、Minimum|
|网络带宽|bit/s|BPS|userId、instanceId|Maximum、 Minimum、 Average|
|EdgeScript规则异常次数|Count|EsCode4xx|userId、instanceId|Sum|
|下行流量|Byte|InternetOut|userId、instanceId|Sum|
|每秒访问次数|Count|QPS|userId、instanceId|Sum|
|返回码4XX占比|%|code4xx|userId、instanceId|Maximum、 Minimum、 Average|
|返回码5XX占比|%|code5xx|userId、instanceId|Maximum、 Minimum、 Average|
|字节命中率|%|hitRate|userId、instanceId|Maximum、 Minimum、 Average|

