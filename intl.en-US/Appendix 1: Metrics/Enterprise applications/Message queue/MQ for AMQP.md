# MQ for AMQP

This topic describes the metrics for Alibaba Cloud Message Queue for AMQP.

-   Set the **Namespace** parameter to **acs\_amqp**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|QueueMessageAccumulation|count/min|QueueMessageAccumulation|userId, regionId, vhostName, and queueName|Maximum|
|QueueMessageInput|count/min|QueueMessageInput|userId, regionId, vhostName, and queueName|Value|
|QueueMessageOutput|count/min|QueueMessageOutput|userId, regionId, vhostName, and queueName|Value|
|VhostMessageInput|count/min|VhostMessageInput|userId, regionId, and vhostName|Value|
|VhostMessageOutput|count/min|VhostMessageOutput|userId, regionId, and vhostName|Value|

