# WAF

This topic describes the metrics for Web Application Firewall.

-   Set the **Namespace** parameter to **WAF**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|4XX\_ratio|%|4XX\_ratio|userId, instanceId, and domain|Maximum|
|5XX\_ratio|%|5XX\_ratio|userId, instanceId, and domain|Maximum|
|acl\_blocks\_5m|count|acl\_blocks\_5m|userId, instanceId, and domain|Maximum|
|acl\_rate\_5m|%|acl\_rate\_5m|userId, instanceId, and domain|Maximum|
|cc\_blocks\_5m|count|cc\_blocks\_5m|userId, instanceId, and domain|Maximum|
|cc\_rate\_5m|%|cc\_rate\_5m|userId, instanceId, and domain|Maximum|
|QPS|countS|qps|userId, instanceId, and domain|Maximum|
|qpsqps\_ratio|%|qps\_ratio|userId, instanceId, and domain|Maximum|
|qps\_ratio\_down|%|qps\_ratio\_down|userId, instanceId, and domain|Maximum|
|waf\_blocks\_5m|count|waf\_blocks\_5m|userId, instanceId, and domain|Maximum|
|waf\_rate\_5m|%|waf\_rate\_5m|userId, instanceId, and domain|Maximum|

