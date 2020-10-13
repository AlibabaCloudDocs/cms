# CDN

通过本文您可以了解CDN的监控项。

-   **Namespace**为**acs\_cdn**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|宽带峰值|bit/s|BPS|userId、instanceId|Maximum、 Minimum、 Average|
|EdgeScript规则异常次数|Count|EsCode4xx|userId、instanceId|Sum|
|下行流量|Byte|InternetOut|userId、instanceId|Sum|
|QPS|Count|QPS|userId、instanceId|Sum|
|返回码4XX占比|%|code4xx|userId、instanceId|Maximum、 Minimum、 Average|
|返回码5XX占比|%|code5xx|userId、instanceId|Maximum、 Minimum、 Average|
|命中率|%|hitRate|userId、instanceId|Maximum、 Minimum、 Average|

