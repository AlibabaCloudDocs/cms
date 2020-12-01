# NewBGPDDoS

This topic describes the metrics of Anti-DDoS Pro.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_newbgpddos**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Active\_Connection|Count|Active\_connection|userId, instanceId, and ip|Maximum|
|Attack\_Traffic|bit/s|AttackTraffic|userId, instanceId, and ip|Maximum|
|Back\_Traffic|bit/s|Back\_Traffic|userId, instanceId, and ip|Maximum|
|In\_Traffic|bit/s|In\_Traffic|userId, instanceId, and ip|Maximum|
|Inactive\_Connection|Count|Inactive\_connection|userId, instanceId, and ip|Maximum|
|New\_Connection|Count|New\_connection|userId, instanceId, and ip|Maximum|
|Out\_Traffic|bit/s|Out\_Traffic|userId, instanceId, and ip|Maximum|
|QPS|CountS|qps|userId, instanceId, and domain|Maximum|
|qps\_ratio\_down|%|qps\_ratio\_down|userId, instanceId, and domain|Maximum|
|qps\_ratio\_up|%|qps\_ratio\_up|userId, instanceId, and domain|Maximum|
|resp2xx|Count|resp2xx|userId, instanceId, and domain|Maximum|
|resp2xx\_ratio|%|resp2xx\_ratio|userId, instanceId, and domain|Maximum|
|resp3xx|Count|resp3xx|userId, instanceId, and domain|Maximum|
|resp3xx\_ratio|%|resp3xx\_ratio|userId, instanceId, and domain|Maximum|
|resp404|Count|resp404|userId, instanceId, and domain|Maximum|
|resp404\_ratio|%|resp404\_ratio|userId, instanceId, and domain|Maximum|
|resp4xx|Count|resp4xx|userId, instanceId, and domain|Maximum|
|resp4xx\_ratio|%|resp4xx\_ratio|userId, instanceId, and domain|Maximum|
|resp5xx|Count|resp5xx|userId, instanceId, and domain|Maximum|
|resp5xx\_ratio|%|resp5xx\_ratio|userId, instanceId, and domain|Maximum|
|upstream\_resp2xx|Count|upstream\_resp2xx|userId, instanceId, and domain|Maximum|
|upstream\_resp2xx\_ratio|%|upstream\_resp2xx\_ratio|userId, instanceId, and domain|Maximum|
|upstream\_resp3xx|Count|upstream\_resp3xx|userId, instanceId, and domain|Maximum|
|upstream\_resp3xx\_ratio|%|upstream\_resp3xx\_ratio|userId, instanceId, and domain|Maximum|
|upstream\_resp404|Count|upstream\_resp404|userId, instanceId, and domain|Maximum|
|upstream\_resp404\_ratio|%|upstream\_resp404\_ratio|userId, instanceId, and domain|Maximum|
|upstream\_resp4xx|Count|upstream\_resp4xx|userId, instanceId, and domain|Maximum|
|upstream\_resp4xx\_ratio|%|upstream\_resp4xx\_ratio|userId, instanceId, and domain|Maximum|
|upstream\_resp5xx|Count|upstream\_resp5xx|userId, instanceId, and domain|Maximum|
|upstream\_resp5xx\_ratio|%|upstream\_resp5xx\_ratio|userId, instanceId, and domain|Maximum|

