# NAT网关

通过本文您可以了解NAT网关的监控项。

-   **Namespace**为**acs\_nat\_gateway**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|SNAT连接数|Count/Min|SnatConnection|userId、instanceId|Maximum|
|历史累积最大限制丢弃连接数|Count/Min|SnatConnectionDrop\_ConcurrentConnectionLimit|userId、instanceId|Maximum|
|历史累积新建限制丢弃连接数|Count/Min|SnatConnectionDrop\_ConnectionRateLimit|userId、instanceId|Maximum|
|并发超规格丢弃速率|countS|SessionLimitDropRate|userId、instanceId|Value|
|新建超规格丢弃速率|countS|SessionNewLimitDropRate|userId、instanceId|Value|
|新建速率|countS|SessionNewConnection2|userId、instanceId|Value|

