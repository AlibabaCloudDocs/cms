# MQ for AMQP Instance

This topic describes the metrics for Alibaba Cloud Message Queue for AMQP instances.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for ApsaraDB for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_amqp**.
-   Set the **Period** parameter to 15s, 60s, or 300s. The default value is 15s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|InstanceConsumers|count|InstanceConsumers|userId, instanceId, and regionId|Value|
|InstanceTpsIn|count/s|InstanceTPSIn|userId, regionId, and instanceId|Value|
|InstanceTpsOut|count/s|InstanceTPSOut|userId, regionId, and instanceId|Value|
|InstanceVhostConsumers|count|InstanceVhostConsumers|userId, instanceId, regionId, and vhostName|Value|
|InstanceVhostQueueConsumers|count|InstanceVhostQueueConsumers|userId, regionId, instanceId, vhostName, and queueName|Value|
|InstanceQueueMessageAccumulation|count|InstanceVhostQueueMessageAccum|userId, regionId, instanceId, queueName, and vhostName|Maximum|
|QueueTPSIn|count/s|QueueTPSIn|userId, regionId, instanceId, queueName, and vhostName|Value|
|QueueTPSOut|count/s|QueueTPSOut|userId, regionId, instanceId, queueName, and vhostName|Value|
|VHostTPSIn|count/s|VHostTPSIn|userId, regionId, instanceId, and vhostName|Value|
|VHostTPSOut|count/s|VHostTPSOut|userId, regionId, instanceId, and vhostName|Value|

