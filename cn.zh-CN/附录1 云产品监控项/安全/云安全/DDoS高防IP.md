# DDoS高防IP

通过本文您可以了解DDoS高防IP的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_ddos**。
-   **Period**默认为60秒，也可以为60的整数倍。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|高防IP活跃并发连接|Count|ActiveConnection|userId、instanceId、ip|Maximum|
|高防IP攻击流量|bit/s|AttackTraffic|userId、instanceId、ip|Maximum|
|高防IP回源带宽|bit/s|BackToSourceTraffic|userId、instanceId、ip|Maximum|
|高防IP非活跃并发连接|Count|InactiveConnection|userId、instanceId、ip|Maximum|
|高防IP入流量|bit/s|InternetInRate|userId、instanceId、ip|Maximum|
|高防IP出流量|bit/s|InternetOutRate|userId、instanceId、ip|Value|
|高防IP新建连接|Count|NewConnection|userId、instanceId、ip|Maximum|

