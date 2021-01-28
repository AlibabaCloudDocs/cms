# Kafka

This topic describes the monitoring metrics of Message Queue for Apache Kafka.

-   Set the **Namespace** parameter to **acs\_kafka**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|InstanceDiskUtilization|%|instance\_disk\_capacity|userId and instanceId|Maximum|
|InstanceMessageInput|bytes/s|instance\_message\_input|userId and instanceId|Value|
|InstanceMessageOutput|bytes/s|instance\_message\_output|userId and instanceId|Value|
|MessageAccumulation|count|message\_accumulation|userId, instanceId, and consumerGroup|Value|
|MessageAccumulationOneTopic|count|message\_accumulation\_onetopic|userId, instanceId, consumerGroup, and topic|Value|
|TopicMessageInput|MB/s|topic\_message\_input|userId, instanceId, and topic|Value|
|TopicMessageOutput|MB/s|topic\_message\_output|userId, instanceId, and topic|Value|

