# 任播弹性公网IP

通过本文您可以了解任播弹性公网IP的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_anycast\_eip**。
-   **Period**默认为60秒，也可以为60的整数倍。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|入方向带宽|bits/s|InboundBandwidth|userId、instanceId、regionNo|Value|
|入方向带宽使用率|Value|InboundBandwidthUsage|userId、instanceId、regionNo|Value|
|入方向包速率|Packets/Second|InboundPacketRate|userId、instanceId、regionNo|Value|
|入方向限速丢包带宽|bits/s|InboundRatelimitDropBandwidth|userId、instanceId、regionNo|Value|
|入方向限速丢包速率|Packets/Second|InboundRatelimitDropSpeed|userId、instanceId、regionNo|Value|
|出方向带宽|bits/s|OutboundBandwidth|userId、instanceId、regionNo|Value|
|出方向带宽使用率|Value|OutboundBandwidthUsage|userId、instanceId、regionNo|Value|
|出方向包速率|Packets/Second|OutboundPacketRate|userId、instanceId、regionNo|Value|
|出方向限速丢包带宽|bits/s|OutboundRatelimitDropBandwidth|userId、instanceId、regionNo|Value|
|出方向限速丢包速率|Packets/Second|OutboundRatelimitDropSpeed|userId、instanceId、regionNo|Value|

