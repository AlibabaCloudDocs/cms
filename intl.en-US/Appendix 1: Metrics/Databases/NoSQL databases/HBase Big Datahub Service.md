# HBase Big Datahub Service

This topic describes the metrics for the data synchronization feature of ApsaraDB for HBase.

-   Set the **Namespace** parameter to **acs\_bds**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|bytes\_in|bytes/s|bytes\_in|userId, instanceId, and host|Average, Maximum, and Minimum|
|bytes\_out|bytes/s|bytes\_out|userId, instanceId, and host|Average, Maximum, and Minimum|
|cold\_storage\_capacity\_bytes|bytes|cold\_storage\_capacity\_bytes|userId, instanceId, and host|Average, Maximum, and Minimum|
|cold\_storage\_used\_bytes|bytes|cold\_storage\_used\_bytes|userId, instanceId, and host|Average, Maximum, and Minimum|
|cold\_storage\_used\_percent|%|cold\_storage\_used\_percent|userId, instanceId, and host|Average, Maximum, and Minimum|
|cpu\_idle|%|cpu\_idle|userId, instanceId, and host|Average, Maximum, and Minimum|
|cpu\_system|%|cpu\_system|userId, instanceId, and host|Average, Maximum, and Minimum|
|cpu\_user|%|cpu\_user|userId, instanceId, and host|Average, Maximum, and Minimum|
|cpu\_wio|%|cpu\_wio|userId, instanceId, and host|Average, Maximum, and Minimum|
|failed\_job\_count|count|failed\_job\_count|userId, instanceId, and host|Average, Maximum, and Minimum|
|load\_five|1|load\_five|userId, instanceId, and host|Average, Maximum, and Minimum|
|load\_one|1|load\_one|userId, instanceId, and host|Average, Maximum, and Minimum|
|mem\_buff\_cache|bytes|mem\_buff\_cache|userId, instanceId, and host|Average, Maximum, and Minimum|
|mem\_free|bytes|mem\_free|userId, instanceId, and host|Average, Maximum, and Minimum|
|mem\_shared|bytes|mem\_shared|userId, instanceId, and host|Average, Maximum, and Minimum|
|mem\_total|bytes|mem\_total|userId, instanceId, and host|Average, Maximum, and Minimum|
|mem\_used\_percent|%|mem\_used\_percent|userId, instanceId, and host|Average, Maximum, and Minimum|
|task\_delay\_max|ms|task\_delay\_max|userId, instanceId, and host|Average, Maximum, and Minimum|
|warn\_job\_count|count|warn\_job\_count|userId, instanceId, and host|Average, Maximum, and Minimum|
|worker\_count|count|worker\_count|userId, instanceId, and host|Average, Maximum, and Minimum|

