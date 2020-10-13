# RocketMQ

This topic describes the metrics for Alibaba Cloud Message Queue for Apache RocketMQ.

-   Set the **Namespace** parameter to **acs\_rocketmq**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|ConsumerLag|count|ConsumerLag|userId, instanceId, and groupId|Sum|
|ConsumerLagPerGidTopic|count|ConsumerLagPerGidTopic|userId, instanceId, groupId, and topic|Sum|
|MessageRetentionPeriod|hour|MessageRetentionPeriod|userId and instanceId|Minimum|
|ReceiveMessageCountPerGid|count/min|ReceiveMessageCountPerGid|userId, instanceId, and groupId|Sum|
|ReceiveMessageCountPerGidTopic|count/min|ReceiveMessageCountPerGidTopic|userId, instanceId, topic, and groupId|Sum|
|Number of messages received by an instance per minute.|count/min|ReceiveMessageCountPerInstance|userId and instanceId|Sum|
|ReceiveMessageCountPerTopic|count/min|ReceiveMessageCountPerTopic|userId, instanceId, and topic|Sum|
|SendDLQMessageCountPerGid|count/min|SendDLQMessageCountPerGid|userId, instanceId, and groupId|Sum|
|SendDLQMessageCountPerGidTopic|count/min|SendDLQMessageCountPerGidTopic|userId, instanceId, groupId, and topic|Sum|
|SendMessageCountPerGid|count/min|SendMessageCountPerGid|userId, instanceId, and groupId|Sum|
|SendMessageCountPerGidTopic|count/min|SendMessageCountPerGidTopic|userId, instanceId, topic, and groupId|Sum|
|SendMessageCountPerInstance|count/min|SendMessageCountPerInstance|userId and instanceId|Sum|
|SendMessageCountPerTopic|count/min|SendMessageCountPerTopic|userId, instanceId, and topic|Sum|

