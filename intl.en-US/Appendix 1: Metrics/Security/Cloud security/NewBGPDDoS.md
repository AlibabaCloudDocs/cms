# NewBGPDDoS

This topic describes the metrics for Anti-DDoS Pro that supports Border Gateway Protocol \(BPG\) bandwidth.

-   Set the **Namespace** parameter to **acs\_newbgpddos**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Active\_connection|count|Active\_connection|userId, instanceId, and ip|Maximum|
|Back\_Traffic|bit/s|Back\_Traffic|userId, instanceId, and ip|Maximum|
|In\_Traffic|bit/s|In\_Traffic|userId, instanceId, and ip|Maximum|
|Inactive\_connection|count|Inactive\_connection|userId, instanceId, and ip|Maximum|
|New\_connection|count|New\_connection|userId, instanceId, and ip|Maximum|
|Out\_Traffic|bit/s|Out\_Traffic|userId, instanceId, and ip|Maximum|

