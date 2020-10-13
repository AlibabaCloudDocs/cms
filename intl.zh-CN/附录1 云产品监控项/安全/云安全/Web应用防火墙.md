# Web应用防火墙

通过本文您可以了解Web应用防火墙的监控项。

-   **Namespace**为**waf**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|4XX占比|%|4XX\_ratio|userId、instanceId、domain|Maximum|
|5XX占比|%|5XX\_ratio|userId、instanceId、domain|Maximum|
|访问控制拦截量（5m）|count|acl\_blocks\_5m|userId、instanceId、domain|Maximum|
|访问控制拦截占比（5m）|%|acl\_rate\_5m|userId、instanceId、domain|Maximum|
|CC防护拦截量（5m）|count|cc\_blocks\_5m|userId、instanceId、domain|Maximum|
|CC防护拦截占比（5m）|%|cc\_rate\_5m|userId、instanceId、domain|Maximum|
|QPS|countS|qps|userId、instanceId、domain|Maximum|
|QPS环比增长率|%|qps\_ratio|userId、instanceId、domain|Maximum|
|QPS环比下降率|%|qps\_ratio\_down|userId、instanceId、domain|Maximum|
|Web攻击拦截量（5m）|count|waf\_blocks\_5m|userId、instanceId、domain|Maximum|
|Web攻击拦截占比（5m）|%|waf\_rate\_5m|userId、instanceId、domain|Maximum|

