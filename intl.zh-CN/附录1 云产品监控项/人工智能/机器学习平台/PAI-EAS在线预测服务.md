# PAI-EAS在线预测服务

通过本文您可以了解PAI-EAS在线预测服务的监控项。

-   **Namespace**为**acs\_learn**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|CPU消耗|count|cpu\_core\_usage|userId、serviceName|Average、Maximum|
|GPU利用率|%|gpu\_util|userId、serviceName|Average、Maximum|
|内存消耗|byte|memory\_rss|userId、serviceName|Average、Maximum、Minimum|
|每秒总调用次数|frequency|qps\_total|userId、serviceName|Value、Average、Maximum|
|状态码2xx每秒响应|frequency|rps\_status\_2xx|userId、serviceName|Average、Maximum、Value、Minimum|
|状态码2xx响应占比|%|rps\_status\_2xx\_ratio|userId、serviceName|Average、Minimum、Maximum、Value|
|状态码4xx每秒响应|frequency|rps\_status\_4xx|userId、instanceId|Average、Maximum、Value|
|状态码4xx响应占比|%|rps\_status\_4xx\_ratio|userId、serviceName|Average、Maximum、Minimum、Value|
|状态码5xx每秒响应|frequency|rps\_status\_5xx|userId、servicName|Average、Maximum、Value|
|状态码5xx响应占比|%|rps\_status\_5xx\_ratio|userId、serviceName|Average、Maximum、Minimum、Value|
|响应时间|microseconds|rt|userId、serviceName|Average、Maximum、Minimum|
|入流量|bps|traffic\_in|userId、serviceName|Average、Maximum、Minimum、Value|
|出流量|bps|traffic\_out|userId、serviceName|Average、Maximum、Minimum、Value|

