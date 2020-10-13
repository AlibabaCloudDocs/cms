# 增强型NAT网关

通过本文您可以了解增强型NAT网关的监控项。

-   **Namespace**为**acs\_nat\_gateway**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|从VPC来流量速率|bps|BWRateInFromInside|userId、instanceId|Value|
|从公网来流量速率|bps|BWRateInFromOutside|userId、instanceId|Value|
|入VPC流量速率|bps|BWRateOutToInside|userId、instanceId|Value|
|入公网流量速率|bps|BWRateOutToOutside|userId、instanceId|Value|
|从VPC来流量|bytes|BytesInFromInside|userId、instanceId|Value|
|从公网来流量|bytes|BytesInFromOutside|userId、instanceId|Value|
|入VPC流量|bytes|BytesOutToInside|userId、instanceId|Value|
|入公网流量|bytes|BytesOutToOutside|userId、instanceId|Value|
|从VPC来包速率|countS|PPSRateInFromInside|userId、instanceId|Value|
|从公网来包速率|countS|PPSRateInFromOutside|userId、instanceId|Value|
|入VPC包速率|countS|PPSRateOutToInside|userId、instanceId|Value|
|入公网包速率|countS|PPSRateOutToOutside|userId、instanceId|Value|
|从VPC来包量|count|PacketsInFromInside|userId、instanceId|Value|
|从公网来包量|count|PacketsInFromOutside|userId、instanceId|Value|
|入VPC包量|count|PacketsOutToInside|userId、instanceId|Value|
|入公网包量|count|PacketsOutToOutside|userId、instanceId|Value|
|并发连接数|count|SessionActiveConnection|userId、instanceId|Value|
|并发连接水位|%|SessionActiveConnectionWaterLever|userId、instanceId|Value|
|并发丢弃连接速率|countS|SessionLimitDropConnection|userId、instanceId|Value|
|新建连接速率|countS|SessionNewConnection|userId、instanceId|Value|
|新建连接水位|%|SessionNewConnectionWaterLever|userId、instanceId|Value|
|新建丢弃连接速率|countS|SessionNewLimitDropConnection|userId、instanceId|Value|

