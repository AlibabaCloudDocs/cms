# ACK \(earlier version\)

This topic describes the metrics for Container Service for Kubernetes \(ACK\).

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_kubernetes**.
-   Set the **Period** parameter to an integral multiple of 60. Default value: 60. Unit: seconds.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|group.cpu.usage\_rate|%|group.cpu.usage\_rate|userId and groupId|Sum|
|group.memory.cache|bytes|group.memory.cache|userId and groupId|Sum|
|group.memory.major\_page\_faults|count|group.memory.major\_page\_faults|userId and groupId|Sum|
|group.memory.major\_page\_faults\_rate|count/s|group.memory.major\_page\_faults\_rate|userId and groupId|Sum|
|group.memory.page\_faults|count|group.memory.page\_faults|userId and groupId|Sum|
|group.memory.page\_faults\_rate|count/s|group.memory.page\_faults\_rate|userId and groupId|Sum|
|group.memory.rss|bytes|group.memory.rss|userId and groupId|Sum|
|group.memory.usage|bytes|group.memory.usage|userId and groupId|Sum|
|group.memory.working\_set|bytes|group.memory.working\_set|userId and groupId|Sum|
|group.network.io\_write\_bytes\_rate|bytes/s|group.network.io\_write\_bytes\_rate|userId and groupId|Sum|
|group.network.rx\_rate|bytes|group.network.rx\_rate|userId and groupId|Sum|
|group.network.tx\_errors|count|group.network.tx\_errors|userId and groupId|Sum|
|group.network.tx\_errors\_rate|count/s|group.network.tx\_errors\_rate|userId and groupId|Sum|
|group.network.tx\_rate|bytes/s|group.network.tx\_rate|userId and groupId|Sum|
|group.uptime|ms|group.uptime|userId and groupId|Sum|
|pod.memory.cache|bytes|pod.memory.cache|userId, groupId, and podId|Average, Maximum, and Minimum|
|pod.memory.major\_page\_faults|count|pod.memory.major\_page\_faults|userId, groupId, and podId|Average, Maximum, and Minimum|
|pod.memory.major\_page\_faults\_rate|count/s|pod.memory.major\_page\_faults\_rate|userId, groupId, and podId|Average, Maximum, and Minimum|
|pod.memory.page\_faults|count|pod.memory.page\_faults|userId, groupId, and podId|Average, Maximum, and Minimum|
|pod.memory.page\_faults\_rate|count/s|pod.memory.page\_faults\_rate|userId, groupId, and podId|Average, Maximum, and Minimum|
|pod.memory.rss|bytes|pod.memory.rss|userId, groupId, and podId|Average, Maximum, and Minimum|
|pod.memory.working\_set|bytes|pod.memory.working\_set|userId, groupId, and podId|Average, Maximum, and Minimum|
|pod.network.io\_write\_bytes\_rate|bytes/s|pod.network.io\_write\_bytes\_rate|userId, groupId, and podId|Average, Maximum, and Minimum|
|pod.network.rx\_errors|count|pod.network.rx\_errors|userId, groupId, and podId|Average, Maximum, and Minimum|
|pod.network.rx\_rate|bytes|pod.network.rx\_rate|userId, groupId, and podId|Average, Maximum, and Minimum|
|pod.uptime|ms|pod.uptime|userId, groupId, and podId|Average, Maximum, and Minimum|
|Memory occupied by the pod|bytes|pod.memory.usage|userId, groupId, and podId|Average, Maximum, and Minimum|
|Inbound traffic errors per second of the pod|count/s|pod.network.rx\_errors\_rate|userId, groupId, and podId|Average, Maximum, and Minimum|
|CPU utilization of the pod|%|pod.cpu.usage\_rate|userId, groupId, and podId|Average, Maximum, and Minimum|
|Outbound traffic per second of the pod|bytes/s|pod.network.tx\_rate|userId, groupId, and podId|Average, Maximum, and Minimum|

