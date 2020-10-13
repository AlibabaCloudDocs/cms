# Alibaba Cloud Container Service for Kubernetes

This topic describes the metrics for Alibaba Cloud Container Service for Kubernetes.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for ApsaraDB for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_kubernetes**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|group.cpu.usage\_rate|%|group.cpu.usage\_rate|userId and groupId|Sum|
|group.memory.cache|byte|group.memory.cache|userId and groupId|Sum|
|group.memory.major\_page\_faults|count|group.memory.major\_page\_faults|userId and groupId|Sum|
|group.memory.major\_page\_faults\_rate|count/s|group.memory.major\_page\_faults\_rate|userId and groupId|Sum|
|group.memory.page\_faults|count|group.memory.page\_faults|userId and groupId|Sum|
|group.memory.page\_faults\_rate|count/s|group.memory.page\_faults\_rate|userId and groupId|Sum|
|group.memory.rss|byte|group.memory.rss|userId and groupId|Sum|
|group.memory.usage|byte|group.memory.usage|userId and groupId|Sum|
|group.memory.working\_set|byte|group.memory.working\_set|userId and groupId|Sum|
|group.network.io\_write\_bytes\_rate|byte/s|group.network.io\_write\_bytes\_rate|userId and groupId|Sum|
|group.network.rx\_rate|byte|group.network.rx\_rate|userId and groupId|Sum|
|group.network.tx\_errors|count|group.network.tx\_errors|userId and groupId|Sum|
|group.network.tx\_errors\_rate|count/s|group.network.tx\_errors\_rate|userId and groupId|Sum|
|group.network.tx\_rate|byte/s|group.network.tx\_rate|userId and groupId|Sum|
|group.uptime|ms|group.uptime|userId and groupId|Sum|
|pod.memory.cache|byte|pod.memory.cache|userId, groupId, and podId|Average, Maximum, and Minimum|
|pod.memory.major\_page\_faults|count|pod.memory.major\_page\_faults|userId, groupId, and podId|Average, Maximum, and Minimum|
|pod.memory.major\_page\_faults\_rate|count/s|pod.memory.major\_page\_faults\_rate|userId, groupId, and podId|Average, Maximum, and Minimum|
|pod.memory.page\_faults|count|pod.memory.page\_faults|userId, groupId, and podId|Average, Maximum, and Minimum|
|pod.memory.page\_faults\_rate|count/s|pod.memory.page\_faults\_rate|userId, groupId, and podId|Average, Maximum, and Minimum|
|pod.memory.rss|byte|pod.memory.rss|userId, groupId, and podId|Average, Maximum, and Minimum|
|pod.memory.working\_set|byte|pod.memory.working\_set|userId, groupId, and podId|Average, Maximum, and Minimum|
|pod.network.io\_write\_bytes\_rate|byte/s|pod.network.io\_write\_bytes\_rate|userId, groupId, and podId|Average, Maximum, and Minimum|
|pod.network.rx\_errors|count|pod.network.rx\_errors|userId, groupId, and podId|Average, Maximum, and Minimum|
|pod.network.rx\_rate|byte|pod.network.rx\_rate|userId, groupId, and podId|Average, Maximum, and Minimum|
|pod.uptime|ms|pod.uptime|userId, groupId, and podId|Average, Maximum, and Minimum|
|Memory occupied by the pod|byte|pod.memory.usage|userId, groupId, and podId|Average, Maximum, and Minimum|
|Inbound traffic errors per second of the pod|count/s|pod.network.rx\_errors\_rate|userId, groupId, and podId|Average, Maximum, and Minimum|
|CPU utilization of the pod|%|pod.cpu.usage\_rate|userId, groupId, and podId|Average, Maximum, and Minimum|
|Outbound traffic per second of the pod|byte/s|pod.network.tx\_rate|userId, groupId, and podId|Average, Maximum, and Minimum|

