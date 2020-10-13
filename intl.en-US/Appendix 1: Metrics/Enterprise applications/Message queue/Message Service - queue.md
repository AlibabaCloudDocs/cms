# Message Service - queue

This topic describes the metrics for queues of Message Service \(MNS\).

-   Set the **Namespace** parameter to **acs\_mns\_new**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|Active Messages|Count|ActiveMessages|userId, region, and queue|Maximum, Minimum, and Average|
|Number of message batch deleting requests|Count|BatchDeleteMessageCount|userId, region, and queue|Maximum, Minimum, and Average|
|Number of message batch receiving requests|Count|BatchReceiveMessageCount|userId, region, and queue|Maximum, Minimum, and Average|
|Number of message batch sending requests|Count|BatchSendMessageCount|userId, region, and queue|Maximum, Minimum, and Average|
|Number of active period modifying requests|Count|ChangeMessageVisibilityCount|userId, region, and queue|Maximum, Minimum, and Average|
|Delayed Message|Count|DelayMessages|userId, region, and queue|Maximum, Minimum, and Average|
|Number of message deleting requests|Count|DeleteMessageCount|userId, region, and queue|Maximum, Minimum, and Average|
|Inactive Messages|Count|InactiveMessages|userId, region, and queue|Maximum, Minimum, and Average|
|Number of message receiving requests|Count|ReceiveMessageCount|userId, region, and queue|Maximum, Minimum, and Average|
|Number of message sending requests|Count|SendMessageCount|userId, region, and queue|Maximum, Minimum, and Average|
|Notification Times|Count|TopicCount|userId, regionName, TopicName, and SubscriptionName|Value|
|Success Rate|%|TopicSuccessRate|userId, regionName, TopicName, and SubscriptionName|Average|

