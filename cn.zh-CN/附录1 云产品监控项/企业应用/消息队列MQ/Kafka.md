# Kafka

通过本文您可以了解消息队列Kafka版的监控项。

-   **Namespace**为**acs\_kafka**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|实例磁盘使用率|%|instance\_disk\_capacity|userId、instanceId|Maximum|
|实例消息生产流量|Bytes/s|instance\_message\_input|userId、instanceId|Value|
|实例消息消费流量|Bytes/s|instance\_message\_output|userId、instanceId|Value|
|消息堆积量|Count|message\_accumulation|userId、instanceId、consumerGroup|Value|
|ConsumerGroup未消费此Topic消息数（个）|Count|message\_accumulation\_onetopic|userId、instanceId、consumerGroup、topic|Value|
|Topic消息生产流量|Mbytes/s|topic\_message\_input|userId、instanceId、topic|Value|
|Topic消息消费流量|Mbytes/s|topic\_message\_output|userId、instanceId、topic|Value|

