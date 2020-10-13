# MQ for AMQP Instance

This topic describes the metrics for Alibaba Cloud Message Queue for AMQP instances.

-   Set the **Namespace** parameter to **acs\_amqp**.
-   Set the **Period** parameter to 15s, 60s, or 300s. The default value is 15s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|InstanceQueueMessageAccumulation|count|InstanceQueueMessageAccumulation|userId, regionId, instanceId, and vhostQueue|Maximum|
|InstanceVhostConsumers|count|InstanceVhostConsumers|userId, regionId, instanceId, and vhostQueue|Value|
|InstanceQueueMessageAccumulation|count|InstanceVhostQueueMessageAccum|userId, regionId, instanceId, queueName, and vhostName|Maximum|

