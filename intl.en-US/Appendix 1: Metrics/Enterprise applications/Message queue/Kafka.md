# Kafka

This topic describes the monitoring metrics of Alibaba Cloud Message Queue for Apache Kafka.

-   Set the **Namespace** parameter to **acs\_kafka**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Item|Unit|Metric|Dimensions|Statistics|
|----|----|------|----------|----------|
|The disk usage of a Message Queue for Apache Kafka instance|%|instance\_disk\_capacity|userId and instanceId|Maximum|
|The production traffic of a Message Queue for Apache Kafka instance|Mbytes/s|instance\_message\_input|userId and instanceId|Value|
|The consumption traffic of a Message Queue for Apache Kafka instance|Mbytes/s|instance\_message\_output|userId and instanceId|Value|
|The number of accumulated messages|Count|message\_accumulation|userId, instanceId, and consumerGroup|Value|
|The number of messages in a topic that are not consumed by the consumer group|Count|message\_accumulation\_onetopic|userId, instanceId, consumerGroup, and topic|Value|
|The production traffic of messages in a topic.|Mbytes/s|topic\_message\_input|userId, instanceId, and topic|Value|
|The consumption traffic of messages in a topic.|Mbytes/s|topic\_message\_output|userId, instanceId, and topic|Value|

