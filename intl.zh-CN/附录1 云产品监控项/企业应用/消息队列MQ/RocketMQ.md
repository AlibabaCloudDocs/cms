# RocketMQ

通过本文您可以了解消息队列RocketMQ版的监控项。

-   **Namespace**为**acs\_rocketmq**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|消息堆积|count|ConsumerLag|userId、instanceId、groupId|Sum|
|消息堆积（GroupID&Topic）|count|ConsumerLagPerGidTopic|userId、instanceId、groupId、topic|Sum|
|消息保留时间|hour|MessageRetentionPeriod|userId、instanceId|Minimum|
|Consumer（GroupId）每分钟接收消息数量|count/min|ReceiveMessageCountPerGid|userId、instanceId、groupId|Sum|
|Consumer（GroupID&Topic）每分钟接收消息数量|count/min|ReceiveMessageCountPerGidTopic|userId、instanceId、topic、groupId|Sum|
|实例\(Instance\) 每分钟接收消息数的数量|count/min|ReceiveMessageCountPerInstance|userId、instanceId|Sum|
|Consumer（GroupId）每分钟接收消息的数量|count/min|ReceiveMessageCountPerTopic|userId、instanceId、topic|Sum|
|每分钟产生死信消息的数量（GroupId）|count/min|SendDLQMessageCountPerGid|userId、instanceId、groupId|Sum|
|每分钟产生死信消息的数量（GroupID&Topic）|count/min|SendDLQMessageCountPerGidTopic|userId、instanceId、groupId、topic|Sum|
|Producer（GroupId）每分钟发送消息的数量|count/min|SendMessageCountPerGid|userId、instanceId、groupId|Sum|
|Producer（GroupID&Topic）每分钟发送消息数量|count/min|SendMessageCountPerGidTopic|userId、instanceId、topic、groupId|Sum|
|实例（Instance）每分钟发送消息数量|count/min|SendMessageCountPerInstance|userId、instanceId|Sum|
|Producer（Topic）每分钟发送消息数量|count/min|SendMessageCountPerTopic|userId、instanceId、topic|Sum|

