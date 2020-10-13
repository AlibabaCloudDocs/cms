# 消息队列AMQP（实例版）

通过本文您可以了解消息队列AMQP版的实例版的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_amqp**。
-   **Period**默认为15秒，也可以为15秒、60秒或300秒。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|Instance消费者数|count|InstanceConsumers|userId、instanceId、regionId|Value|
|Instance消息每秒流入数|countS|InstanceTPSIn|userId、regionId、instanceId|Value|
|Instance消息每秒流出数|countS|InstanceTPSOut|userId、regionId、instanceId|Value|
|VHost消费者数量|count|InstanceVhostConsumers|userId、instanceId、regionId、vhostName|Value|
|Queue消费者数量|count|InstanceVhostQueueConsumers|userId、regionId、instanceId、vhostName、queueName|Value|
|Queue消息堆积量|count|InstanceVhostQueueMessageAccum|userId、regionId、instanceId、queueName、vhostName|Maximum|
|Queue每秒消息流入数|countS|QueueTPSIn|userId、regionId、instanceId、vhostName、queueName|Value|
|Queue每秒消息流出数|countS|QueueTPSOut|userId、regionId、instanceId、vhostName、queueName|Value|
|VHost每秒消息流入数|countS|VHostTPSIn|userId、regionId、instanceId、vhostName|Value|
|VHost每秒消息流出数|countS|VHostTPSOut|userId、regionId、instanceId、vhostName|Value|

