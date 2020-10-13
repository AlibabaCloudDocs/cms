# 容器服务Kubernetes版

通过本文您可以了解容器服务Kubernetes版的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_kubernetes**。
-   **Period**默认为60秒，也可以为60的整数倍。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|group.cpu.usage\_rate|%|group.cpu.usage\_rate|userId、groupId|Sum|
|group.memory.cache|bytes|group.memory.cache|userId、groupId|Sum|
|group.memory.major\_page\_faults|count|group.memory.major\_page\_faults|userId、groupId|Sum|
|group.memory.major\_page\_faults\_rate|count/s|group.memory.major\_page\_faults\_rate|userId、groupId|Sum|
|group.memory.page\_faults|count|group.memory.page\_faults|userId、groupId|Sum|
|group.memory.page\_faults\_rate|count/s|group.memory.page\_faults\_rate|userId、groupId|Sum|
|group.memory.rss|bytes|group.memory.rss|userId、groupId|Sum|
|group.memory.usage|bytes|group.memory.usage|userId、groupId|Sum|
|group.memory.working\_set|bytes|group.memory.working\_set|userId、groupId|Sum|
|group.network.io\_write\_bytes\_rate|bytes/s|group.network.io\_write\_bytes\_rate|userId、groupId|Sum|
|group.network.rx\_rate|bytes|group.network.rx\_rate|userId、groupId|Sum|
|group.network.tx\_errors|count|group.network.tx\_errors|userId、groupId|Sum|
|group.network.tx\_errors\_rate|count/s|group.network.tx\_errors\_rate|userId、groupId|Sum|
|group.network.tx\_rate|bytes/s|group.network.tx\_rate|userId、groupId|Sum|
|group.uptime|ms|group.uptime|userId、groupId|Sum|
|pod.memory.cache|bytes|pod.memory.cache|userId、groupId、podId|Average、Maximum、Minimum|
|pod.memory.major\_page\_faults|count|pod.memory.major\_page\_faults|userId、groupId、podId|Average、Maximum、Minimum|
|pod.memory.major\_page\_faults\_rate|count/s|pod.memory.major\_page\_faults\_rate|userId、groupId、podId|Average、Maximum、Minimum|
|pod.memory.page\_faults|count|pod.memory.page\_faults|userId、groupId、podId|Average、Maximum、Minimum|
|pod.memory.page\_faults\_rate|count/s|pod.memory.page\_faults\_rate|userId、groupId、podId|Average、Maximum、Minimum|
|pod.memory.rss|bytes|pod.memory.rss|userId、groupId、podId|Average、Maximum、Minimum|
|pod.memory.working\_set|bytes|pod.memory.working\_set|userId、groupId、podId|Average、Maximum、Minimum|
|pod.network.io\_write\_bytes\_rate|bytes/s|pod.network.io\_write\_bytes\_rate|userId、groupId、podId|Average、Maximum、Minimum|
|pod.network.rx\_errors|count|pod.network.rx\_errors|userId、groupId、podId|Average、Maximum、Minimum|
|pod.network.rx\_rate|bytes|pod.network.rx\_rate|userId、groupId、podId|Average、Maximum、Minimum|
|pod.uptime|ms|pod.uptime|userId、groupId、podId|Average、Maximum、Minimum|
|内存使用量|bytes|pod.memory.usage|userId、groupId、podId|Average、Maximum、Minimum|
|容器组网络流入错误比例|count/s|pod.network.rx\_errors\_rate|userId、groupId、podId|Average、Maximum、Minimum|
|容器组使用率|%|pod.cpu.usage\_rate|userId、groupId、podId|Average、Maximum、Minimum|
|容器组网络流出比例|bytes/s|pod.network.tx\_rate|userId、groupId、podId|Average、Maximum、Minimum|

