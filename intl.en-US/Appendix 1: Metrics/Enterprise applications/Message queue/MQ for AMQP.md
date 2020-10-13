# MQ for AMQP

This topic describes the metrics for Alibaba Cloud Message Queue for AMQP.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for ApsaraDB for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_amqp**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|QueueMessageAccumulation|count/min|QueueMessageAccumulation|userId, regionId, vhostName, and queueName|Maximum|
|QueueMessageInput|count/min|QueueMessageInput|userId, regionId, vhostName, and queueName|Value|
|QueueMessageOutput|count/min|QueueMessageOutput|userId, regionId, vhostName, and queueName|Value|
|VhostMessageInput|count/min|VhostMessageInput|userId, regionId, and vhostName|Value|
|VhostMessageOutput|count/min|VhostMessageOutput|userId, regionId, and vhostName|Value|

