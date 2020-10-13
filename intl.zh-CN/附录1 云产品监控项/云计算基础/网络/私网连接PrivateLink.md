# 私网连接PrivateLink

通过本文您可以了解私网连接PrivateLink的监控项。

-   **Namespace**为**acs\_privatelink**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|终端节点弹性网卡流入带宽|bit/s|EndpointENIInBps|userId、instanceId、eniId|Average|
|终端节点弹性网卡流入丢弃带宽|bit/s|EndpointENIInDropBps|userId、instanceId、eniId|Average|
|终端节点弹性网卡流入丢弃数据包速率|packet/s|EndpointENIInDropPps|userId、instanceId、eniId|Average|
|终端节点弹性网卡流入数据包速率|packet/s|EndpointENIInPps|userId、instanceId、eniId|Average|
|终端节点弹性网卡流出带宽|bit/s|EndpointENIOutBps|userId、instanceId、eniId|Average|
|终端节点弹性网卡流出丢弃带宽|bit/s|EndpointENIOutDropBps|userId、instanceId、eniId|Average|
|终端节点弹性网卡流出丢弃数据包速率|packet/s|EndpointENIOutDropPps|userId、instanceId、eniId|Average|
|终端节点弹性网卡流出数据包速率|packet/s|EndpointENIOutPps|userId、instanceId、eniId|Average|
|终端节点流入带宽|bit/s|EndpointInBps|userId、instanceId|Average|
|终端节点流入丢弃带宽|bit/s|EndpointInDropBps|userId、instanceId|Average|
|终端节点流入丢弃数据包速率|packet/s|EndpointInDropPps|userId、instanceId|Average|
|终端节点流入数据包速率|packet/s|EndpointInPps|userId、instanceId|Average|
|终端节点流出带宽|bit/s|EndpointOutBps|userId、instanceId|Average|
|终端节点流出丢弃带宽|bit/s|EndpointOutDropBps|userId、instanceId|Average|
|终端节点流出丢弃数据包速率|packet/s|EndpointOutDropPps|userId、instanceId|Average|
|终端节点流出数据包速率|packet/s|EndpointOutPps|userId、instanceId|Average|

