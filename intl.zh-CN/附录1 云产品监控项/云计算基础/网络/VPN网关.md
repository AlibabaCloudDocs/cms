# VPN网关

通过本文您可以了解VPN网关的监控项。

-   **Namespace**为**acs\_vpn**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|连接流入包速率|pps|ipsec.rxPkgs|userId、instanceId、ipsecId|Value|
|连接流出包速率|pps|ipsec.txPkgs|userId、instanceId、ipsecId|Value|
|连接流入带宽|bits/s|ipsec\_rx.rate|userId、instanceId、ipsecId|Value|
|连接流出带宽|bits/s|ipsec\_tx.rate|userId、instanceId、ipsecId|Value|
|流入带宽|bits/s|net\_rx.rate|userId、instanceId|Value|
|流出带宽|bits/s|net\_tx.rate|userId、instanceId|Value|
|连接个数|count|ssl\_client.count|userId、instanceId|Value|
|网关流入包速率|pps|net\_rx.Pkgs|userId、instanceId|Value|
|网关流出包速率|pps|net\_tx.Pkgs|userId、instanceId|Value|

