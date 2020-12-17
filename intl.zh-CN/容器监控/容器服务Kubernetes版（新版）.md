# 容器服务Kubernetes版（新版）

通过本文您可以了解容器服务Kubernetes版的集群、节点、命名空间、应用和容器组的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_k8s**。
-   **Period**默认为60秒，也可以为60的整数倍。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|cluster.cpu.allocatable|cores|cluster.cpu.allocatable|userId、cluster|Value|
|cluster.cpu.limit|cores|cluster.cpu.limit|userId、cluster|Value|
|cluster.cpu.request|cores|cluster.cpu.request|userId、cluster|Value|
|cluster.cpu.usage\_rate|cores|cluster.cpu.usage\_rate|userId、cluster|Value|
|cluster.memory.allocatable|Bytes|cluster.memory.allocatable|userId、cluster|Value|
|cluster.memory.limit|Bytes|cluster.memory.limit|userId、cluster|Value|
|cluster.memory.request|Bytes|cluster.memory.request|userId、cluster|Value|
|ns.cpu.limit|cores|ns.cpu.limit|userId、cluster、namespace|Sum|
|ns.cpu.request|cores|ns.cpu.request|userId、cluster、namespace|Sum|
|ns.cpu.usage\_rate|cores|ns.cpu.usage\_rate|userId、cluster、namespace|Sum|
|ns.memory.limit|bytes|ns.memory.limit|userId、cluster、namespace|Sum|
|ns.memory.request|bytes|ns.memory.request|userId、cluster、namespace|Sum|
|ns.memory.usage|%|ns.memory.usage|userId、cluster、namespace|Average、Maximum、Minimum、Sum、Count、Value|
|ns.memory.working\_set|bytes|ns.memory.working\_set|userId、cluster、namespace|Sum|
|node.cpu.allocatable|cores|node.cpu.allocatable|userId、cluster、node|Value|
|node.cpu.capacity|cores|node.cpu.capacity|userId、cluster、node|Value|
|node.cpu.limit|cores|node.cpu.limit|userId、cluster、node|Value|
|node.cpu.request|cores|node.cpu.request|userId、cluster、node|Value|
|node.cpu.reservation|cores|node.cpu.reservation|userId、cluster、node|Value|
|node.cpu.usage\_rate|cores|node.cpu.usage\_rate|userId、cluster、node|Value|
|node.cpu.utilization|%|node.cpu.utilization|userId、cluster、node|Value|
|node.filesystem.available|count|node.filesystem.available|userId、cluster、node|Value|
|node.filesystem.inodes|count|node.filesystem.inodes|userId、cluster、node|Value|
|node.filesystem.limit|count|node.filesystem.limit|userId、cluster、node|Value|
|node.filesystem.usage|count|node.filesystem.usage|userId、cluster、node|Value|
|node.memory.allocatable|Bytes|node.memory.allocatable|userId、cluster、node|Value|
|node.memory.cache|count|node.memory.cache|userId、cluster、node|Value|
|node.memory.capacity|count|node.memory.capacity|userId、cluster、node|Value|
|node.memory.limit|count|node.memory.limit|userId、cluster、node|Value|
|node.memory.major\_page\_faults|count|node.memory.major\_page\_faults|userId、cluster、node|Value|
|node.memory.major\_page\_faults\_rate|count|node.memory.major\_page\_faults\_rate|userId、cluster、node|Value|
|node.memory.page\_faults|count|node.memory.page\_faults|userId、cluster、node|Value|
|node.memory.page\_faults\_rate|count|node.memory.page\_faults\_rate|userId、cluster、node|Value|
|node.memory.request|count|node.memory.request|userId、cluster、node|Value|
|node.memory.reservation|count|node.memory.reservation|userId、cluster、node|Value|
|node.memory.rss|count|node.memory.rss|userId、cluster、node|Value|
|node.memory.usage|count|node.memory.usage|userId、cluster、node|Value|
|node.memory.utilization|%|node.memory.utilization|userId、cluster、node|Value|
|node.memory.working\_set|count|node.memory.working\_set|userId、cluster、node|Value|
|node.network.rx\_errors|count|node.network.rx\_errors|userId、cluster、node|Value|
|node.network.rx\_errors\_rate|count|node.network.rx\_errors\_rate|userId、cluster、node|Value|
|node.network.rx\_rate|count|node.network.rx\_rate|userId、cluster、node|Value|
|node.network.tx\_errors\_rate|count|node.network.tx\_errors\_rate|userId、cluster、node|Value|
|node.network.tx\_rate|count|node.network.tx\_rate|userId、cluster、node|Value|
|部署应用CPU资源分配上限|cores|deployment.cpu.limit|userId、cluster、namespace、type、app|Sum|
|部署应用CPU资源分配最小需求|cores|deployment.cpu.request|userId、cluster、namespace、type、app|Sum|
|部署应用CPU使用量|cores|deployment.cpu.usage\_rate|userId、cluster、namespace、type、app|Sum|
|部署应用内存资源分配上限|bytes|deployment.memory.limit|userId、cluster、namespace、type、app|Sum|
|部署应用内存资源分配最小需求|bytes|deployment.memory.request|userId、cluster、namespace、type、app|Sum|
|部署应用工作内存使用量|bytes|deployment.memory.working\_set|userId、cluster、namespace、type、app|Sum|
|部署应用网络接收速率|bytes/s|deployment.network.rx\_rate|userId、cluster、namespace、type、app|Sum|
|部署应用网络发送速率|bytes/s|deployment.network.tx\_rate|userId、cluster、namespace、type、app|Sum|
|容器组CPU资源分配上限|cores|pod.cpu.limit|userId、cluster、namespace、type、app、pod|Value|
|容器组CPU资源分配最小需求|cores|pod.cpu.request|userId、cluster、namespace、type、app、pod|Value|
|容器组CPU使用量|cores|pod.cpu.usage\_rate|userId、cluster、namespace、type、app、pod|Value|
|容器组内存资源分配上限|bytes|pod.memory.limit|userId、cluster、namespace、type、app、pod|Value|
|容器组内存资源分配最小需求|bytes|pod.memory.request|userId、cluster、namespace、type、app、pod|Value|
|容器组工作内存使用量|bytes|pod.memory.working\_set|userId、cluster、namespace、type、app、pod|Value|
|容器组网络接收错误速率|bytes/s|pod.network.rx\_errors\_rate|userId、cluster、namespace、type、app、pod|Value|
|容器组网络接受速率|bytes/s|pod.network.rx\_rate|userId、cluster、namespace、type、app、pod|Value|
|容器组网络发送错误速率|bytes/s|pod.network.tx\_errors\_rate|userId、cluster、namespace、type、app、pod|Value|
|容器组网络发送速率|bytes/s|pod.network.tx\_rate|userId、cluster、namespace、type、app、pod|Value|

