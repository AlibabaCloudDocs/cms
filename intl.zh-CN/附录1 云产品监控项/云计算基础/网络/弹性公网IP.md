# 弹性公网IP

通过本文您可以了解弹性公网IP的监控项。

-   **Namespace**为**acs\_vpc\_eip**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|网络入流量|Byte|net.rx|userld、instanceld|Average、Minimum、Maximum、Sum|
|流入数据包数|Count|net.rxPkgs|userld、instanceld|Average、Minimum、Maximum、Sum|
|网络出流量|Byte|net.tx|userld、instanceld|Average、Minimum、Maximum、Sum|
|流出数据包数|Count|net.txPkgs|userld、instanceld|Average、Minimum、Maximum、Sum|
|流入带宽|bit/s|net\_rx.rate|userld、instanceld|Value|
|流入包速率|Packets/Second|net\_rxPkgs.rate|userld、instanceld|Value|
|流出带宽|bit/s|net\_tx.rate|userld、instanceld|Value|
|流出包速率|Packets/Second|net\_txPkgs.rate|userld、instanceld|Value|
|限速丢包速率|Packets/Second|out\_ratelimit\_drop\_speed|userld、instanceld|Average|
|网络流入带宽利用率|%|net\_in.rate\_percentage|userld、instanceld|Average、Minimum、Maximum、|
|网络流出带宽利用率|%|net\_out.rate\_percentage|userld、instanceld|Average、Minimum、Maximum、|

