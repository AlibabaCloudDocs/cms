# 消息队列AMQP

通过本文您可以了解消息队列AMQP版的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_amqp**。
-   **Period**默认为60秒，也可以为60的整数倍。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|queue消息堆积数量|count/min|QueueMessageAccumulation|userId、regionId、vhostName、queueName|Maximum|
|queue消息生产数量|count/min|QueueMessageInput|userId、regionId、vhostName、queueName|Value|
|queue消息消费数量|count/min|QueueMessageOutput|userId、regionId、vhostName、queueName|Value|
|vhost消息生产数量|count/min|VhostMessageInput|userId、regionId、vhostName|Value|
|vhost消息消费数量|count/min|VhostMessageOutput|userId、regionId、vhostName|Value|

