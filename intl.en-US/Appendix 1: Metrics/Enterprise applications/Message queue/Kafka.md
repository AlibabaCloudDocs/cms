# Kafka

This topic describes the metrics for Alibaba Cloud Message Queue for Apache Kafka.

-   Set the **Namespace** parameter to**acs\_kafka**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|InstanceDiskUtilization|%|instance\_disk\_capacity|userId and instanceId|Maximum|
|InstanceMessageInput|Mbytes/s|instance\_message\_input|userId and instanceId|Value|
|InstanceMessageOutput|Mbytes/s|instance\_message\_output|userId and instanceId|Value|
|MessageAccumulation|Count|message\_accumulation|userId, instanceId, and consumerGroup|Value|
|MessageAccumulationOneTopic|Count|message\_accumulation-onetopic|userId, instanceId, consumerGroup, and topic|Value|
|TopicMessageInput|Mbytes/s|topic\_message\_input|userId, instanceId, and topic|Value|
|TopicMessageOutput|Mbytes/s|topic\_message\_output|userId, instanceId, and topic|Value|

