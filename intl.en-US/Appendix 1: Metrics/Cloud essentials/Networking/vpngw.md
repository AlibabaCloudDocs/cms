# vpngw

This topic describes the metrics for VPN Gateway.

-   Set the **Namespace** parameter to **acs\_vpn**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Inbound Packages|packet/s|ipsec.rxPkgs|userId, instanceId, and ipsecId|Value|
|Outbound Packages|packet/s|ipsec.txPkgs|userId, instanceId, and ipsecId|Value|
|Inbound Bandwidth|bit/s|ipsec\_rx.rate|userId, instanceId, and ipsecId|Value|
|Outbound Bandwidth|bit/s|ipsec\_tx.rate|userId, instanceId, and ipsecId|Value|
|Inbound Bandwidth|bit/s|net\_rx.rate|userId and instanceId|Value|
|Outbound Bandwidth|bit/s|net\_tx.rate|userId and instanceId|Value|
|SSL Client Count|count|ssl\_client.count|userId and instanceId|Value|
|Gateway.rxPkgs|packet/s|net\_rx.Pkgs|userId and instanceId|Value|
|Gateway.txPkgs|packet/s|net\_tx.Pkgs|userId and instanceId|Value|

