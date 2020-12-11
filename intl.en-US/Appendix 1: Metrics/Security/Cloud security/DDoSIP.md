# DDoSIP

This topic describes the metrics of Anti-DDoS Pro.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_ddos**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Active\_connection|Count|ActiveConnection|userId, instanceId, and ip|Maximum|
|AttackTraffic|bit/s|AttackTraffic|userId, instanceId, and ip|Maximum|
|Back\_Traffic|bit/s|BackToSourceTraffic|userId, instanceId, and ip|Maximum|
|Inactive\_connection|Count|InactiveConnection|userId, instanceId, and ip|Maximum|
|In\_Traffic|bit/s|InternetInRate|userId, instanceId, and ip|Maximum|
|Out\_Traffic|bit/s|InternetOutRate|userId, instanceId, and ip|Value|
|New\_connection|Count|NewConnection|userId, instanceId, and ip|Maximum|

