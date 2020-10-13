# DDOS

This topic describes the metrics for Anti-DDoS Pro.

-   Set the **Namespace** parameter to **acs\_ddos**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Active\_connection|count|ActiveConnection|userId, instanceId, and ip|Maximum|
|AttackTraffic|bit/s|AttackTraffic|userId, instanceId, and ip|Maximum|
|Back\_Traffic|bit/s|BackToSourceTraffic|userId, instanceId, and ip|Maximum|
|Inactive\_connection|count|InactiveConnection|userId, instanceId, and ip|Maximum|
|In\_Traffic|bit/s|InternetInRate|userId, instanceId, and ip|Maximum|
|Out\_Traffic|bit/s|InternetOutRate|userId, instanceId, and ip|Value|
|New\_connection|count|NewConnection|userId, instanceId, and ip|Maximum|

