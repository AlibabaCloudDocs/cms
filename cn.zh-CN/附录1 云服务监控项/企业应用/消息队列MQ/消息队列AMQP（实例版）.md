# 消息队列AMQP（实例版）

通过本文您可以了解消息队列AMQP版的实例版的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_amqp**。
-   **Period**默认为15秒，也可以为15秒、60秒或300秒。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|Exchange每秒消息流入数|CountS|ExchangeTPSIn|userId、regionId、instanceId、vhostName、exchangeName|Value|
|Exchange每秒消息流出数|CountS|ExchangeTPSOut|userId、regionId、instanceId、vhostName、exchangeName|Value|
|Instance的Channel数量|Count|InstanceChannels|userId、instanceId、regionId|Sum|
|Instance通道数量|Count|InstanceChannelsNew|userId、instanceId、regionId|Value|
|Instance连接数量|Count|InstanceConnections|userId、instanceId、regionId|Value|
|Instance消费者数|Count|InstanceConsumers|userId、instanceId、regionId|Value|
|Instance消息生产数量|Count|InstanceMessageInput|userId、regionId、instanceId|Sum|
|Instance消息消费数量|Count|InstanceMessageOutput|userId、regionId、instanceId|Sum|
|Instance消息每秒流入数|CountS|InstanceTPSIn|userId、regionId、instanceId|Value|
|Instance消息每秒流出数|CountS|InstanceTPSOut|userId、regionId、instanceId|Value|
|Instance每秒消息流入峰值|CountS|InstanceTopTPSIn|userId、regionId、instanceId|Value|
|Instance每秒消息流出峰值|CountS|InstanceTopTPSOut|userId、regionId、instanceId|Value|
|VHost的Channel 数|Count|InstanceVhostChannels|userId、instanceId、vhostName、regionId|Sum|
|VHost消费者数量|Count|InstanceVhostConsumers|userId、instanceId、regionId、vhostName|Value|
|Queue消费者数量|Count|InstanceVhostQueueConsumers|userId、regionId、instanceId、vhostName、queueName|Value|
|Queue消息堆积量|Count|InstanceVhostQueueMessageAccum|userId、regionId、instanceId、queueName、vhostName|Maximum|
|Queue消息生产数量|Count|InstanceVhostQueueMessageInput|userId、regionId、instanceId、vhostName、queueName|Sum|
|Queue消息消费数量|Count|InstanceVhostQueueMessageOutput|userId、regionId、instanceId、vhostName、queueName|Sum|
|Queue消息堆积数量|Count/min|QueueMessageAccumulation|userId、regionId、vhostName、queueName|Maximum|
|Queue消息生产数量|Count/min|QueueMessageInput|userId、regionId、vhostName、queueName|Value|
|Queue消息消费数量|Count/min|QueueMessageOutput|userId、regionId、vhostName、queueName|Value|
|Queue消息每秒流入数|CountS|QueueTPSIn|userId、regionId、instanceId、vhostName、queueName|Value|
|Queue每秒消息流出数|CountS|QueueTPSOut|userId、regionId、instanceId、vhostName、queueName|Value|
|Queue每秒消息流入峰值|CountS|QueueTopTPSIn|userId、regionId、instanceId、vhostName、queueName|Value|
|Queue每秒消息流出峰值|CountS|QueueTopTPSOut|userId、regionId、instanceId、vhostName、queueName|Value|
|VHost每秒消息流入数|CountS|VHostTPSIn|userId、regionId、instanceId、vhostName|Value|
|VHost每秒消息流出数|CountS|VHostTPSOut|userId、regionId、instanceId、vhostName|Value|
|VHost每秒消息流入峰值|CountS|VHostTopTPSIn|userId、regionId、instanceId、vhostName|Value|
|VHost每秒消息流出峰值|CountS|VHostTopTPSOut|userId、regionId、instanceId、vhostName|Value|
|VHost通道数量|Count|VhostChannels|userId、instanceId、regionId、vhostName|Value|
|VHost连接数量|Count|VhostConnections|userId、instanceId、regionId、vhostName|Value|
|Vhost消息生产数量|Count/min|VhostMessageInput|userId、regionId、vhostName|Value|
|Vhost消息消费数量|Count/min|VhostMessageOutput|userId、regionId、vhostName|Value|

