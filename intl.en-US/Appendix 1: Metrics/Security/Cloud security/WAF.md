# WAF

This topic describes the metrics of Web Application Firewall \(WAF\).

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **waf**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|4XX\_ratio|%|4XX\_ratio|userId, instanceId, and domain|Maximum|
|5XX\_ratio|%|5XX\_ratio|userId, instanceId, and domain|Maximum|
|acl\_blocks\_5m|Count|acl\_blocks\_5m|userId, instanceId, and domain|Maximum|
|acl\_rate\_5m|%|acl\_rate\_5m|userId, instanceId, and domain|Maximum|
|cc\_blocks\_5m|Count|cc\_blocks\_5m|userId, instanceId, and domain|Maximum|
|cc\_rate\_5m|%|cc\_rate\_5m|userId, instanceId, and domain|Maximum|
|QPS|CountS|qps|userId, instanceId, and domain|Maximum|
|qps\_ratio|%|qps\_ratio|userId, instanceId, and domain|Maximum|
|qps\_ratio\_down|%|qps\_ratio\_down|userId, instanceId, and domain|Maximum|
|waf\_blocks\_5m|Count|waf\_blocks\_5m|userId, instanceId, and domain|Maximum|
|waf\_rate\_5m|%|waf\_rate\_5m|userId, instanceId, and domain|Maximum|

