# ACK \(new version\)

This topic describes the metrics for clusters, nodes, namespaces, applications, and pods in Container Service for Kubernetes \(ACK\).

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_k8s**.
-   Set the **Period** parameter to an integral multiple of 60. Default value: 60. Unit: seconds.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|cluster.cpu.allocatable|cores|cluster.cpu.allocatable|userId and cluster|Value|
|cluster.cpu.limit|cores|cluster.cpu.limit|userId and cluster|Value|
|cluster.cpu.request|cores|cluster.cpu.request|userId and cluster|Value|
|cluster.cpu.usage\_rate|cores|cluster.cpu.usage\_rate|userId and cluster|Value|
|cluster.memory.allocatable|Bytes|cluster.memory.allocatable|userId and cluster|Value|
|cluster.memory.limit|Bytes|cluster.memory.limit|userId and cluster|Value|
|cluster.memory.request|Bytes|cluster.memory.request|userId and cluster|Value|
|ns.cpu.limit|cores|ns.cpu.limit|userId, cluster, and namespace|Sum|
|ns.cpu.request|cores|ns.cpu.request|userId, cluster, and namespace|Sum|
|ns.cpu.usage\_rate|cores|ns.cpu.usage\_rate|userId, cluster, and namespace|Sum|
|ns.memory.limit|bytes|ns.memory.limit|userId, cluster, and namespace|Sum|
|ns.memory.request|bytes|ns.memory.request|userId, cluster, and namespace|Sum|
|ns.memory.usage|%|ns.memory.usage|userId, cluster, and namespace|Average, Maximum, Minimum, Sum, Count, and Value|
|ns.memory.working\_set|bytes|ns.memory.working\_set|userId, cluster, and namespace|Sum|
|node.cpu.allocatable|cores|node.cpu.allocatable|userId, cluster, and node|Value|
|node.cpu.capacity|cores|node.cpu.capacity|userId, cluster, and node|Value|
|node.cpu.limit|cores|node.cpu.limit|userId, cluster, and node|Value|
|node.cpu.request|cores|node.cpu.request|userId, cluster, and node|Value|
|node.cpu.reservation|cores|node.cpu.reservation|userId, cluster, and node|Value|
|node.cpu.usage\_rate|cores|node.cpu.usage\_rate|userId, cluster, and node|Value|
|node.cpu.utilization|%|node.cpu.utilization|userId, cluster, and node|Value|
|node.filesystem.available|count|node.filesystem.available|userId, cluster, and node|Value|
|node.filesystem.inodes|count|node.filesystem.inodes|userId, cluster, and node|Value|
|node.filesystem.limit|count|node.filesystem.limit|userId, cluster, and node|Value|
|node.filesystem.usage|count|node.filesystem.usage|userId, cluster, and node|Value|
|node.memory.allocatable|Bytes|node.memory.allocatable|userId, cluster, and node|Value|
|node.memory.cache|count|node.memory.cache|userId, cluster, and node|Value|
|node.memory.capacity|count|node.memory.capacity|userId, cluster, and node|Value|
|node.memory.limit|count|node.memory.limit|userId, cluster, and node|Value|
|node.memory.major\_page\_faults|count|node.memory.major\_page\_faults|userId, cluster, and node|Value|
|node.memory.major\_page\_faults\_rate|count|node.memory.major\_page\_faults\_rate|userId, cluster, and node|Value|
|node.memory.page\_faults|count|node.memory.page\_faults|userId, cluster, and node|Value|
|node.memory.page\_faults\_rate|count|node.memory.page\_faults\_rate|userId, cluster, and node|Value|
|node.memory.request|count|node.memory.request|userId, cluster, and node|Value|
|node.memory.reservation|count|node.memory.reservation|userId, cluster, and node|Value|
|node.memory.rss|count|node.memory.rss|userId, cluster, and node|Value|
|node.memory.usage|count|node.memory.usage|userId, cluster, and node|Value|
|node.memory.utilization|%|node.memory.utilization|userId, cluster, and node|Value|
|node.memory.working\_set|count|node.memory.working\_set|userId, cluster, and node|Value|
|node.network.rx\_errors|count|node.network.rx\_errors|userId, cluster, and node|Value|
|node.network.rx\_errors\_rate|count|node.network.rx\_errors\_rate|userId, cluster, and node|Value|
|node.network.rx\_rate|count|node.network.rx\_rate|userId, cluster, and node|Value|
|node.network.tx\_errors\_rate|count|node.network.tx\_errors\_rate|userId, cluster, and node|Value|
|node.network.tx\_rate|count|node.network.tx\_rate|userId, cluster, and node|Value|
|CPU resource limit of resources|cores|deployment.cpu.limit|userId, cluster, namespace, type, and app|Sum|
|CPU resource request of resources|cores|deployment.cpu.request|userId, cluster, namespace, type, and app|Sum|
|CPU usage of resources|cores|deployment.cpu.usage\_rate|userId, cluster, namespace, type, and app|Sum|
|Memory resource limit of resources|bytes|deployment.memory.limit|userId, cluster, namespace, type, and app|Sum|
|Memory resource request of resources|bytes|deployment.memory.request|userId, cluster, namespace, type, and app|Sum|
|Memory working set of resources|bytes|deployment.memory.working\_set|userId, cluster, namespace, type, and app|Sum|
|Network inflow ratio of resources|bytes/s|deployment.network.rx\_rate|userId, cluster, namespace, type, and app|Sum|
|Network outflow ratio of resources|bytes/s|deployment.network.tx\_rate|userId, cluster, namespace, type, and app|Sum|
|CPU resource limit of container group|cores|pod.cpu.limit|userId, cluster, namespace, type, app, and pod|Value|
|CPU resource request of container group|cores|pod.cpu.request|userId, cluster, namespace, type, app, and pod|Value|
|CPU usage of container group|cores|pod.cpu.usage\_rate|userId, cluster, namespace, type, app, and pod|Value|
|Memory resource limit of container group|bytes|pod.memory.limit|userId, cluster, namespace, type, app, and pod|Value|
|Memory resource request of container group|bytes|pod.memory.request|userId, cluster, namespace, type, app, and pod|Value|
|Memory working set of container group|bytes|pod.memory.working\_set|userId, cluster, namespace, type, app, and pod|Value|
|Network inflow error ratio of container group|bytes/s|pod.network.rx\_errors\_rate|userId, cluster, namespace, type, app, and pod|Value|
|Network inflow ratio of container group|bytes/s|pod.network.rx\_rate|userId, cluster, namespace, type, app, and pod|Value|
|Network outflow error ratio of container group|bytes/s|pod.network.tx\_errors\_rate|userId, cluster, namespace, type, app, and pod|Value|
|Network outflow ratio of container group|bytes/s|pod.network.tx\_rate|userId, cluster, namespace, type, app, and pod|Value|

