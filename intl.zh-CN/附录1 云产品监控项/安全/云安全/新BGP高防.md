# 新BGP高防

通过本文您可以了解DDoS高防的新BGP的监控项。

-   **Namespace**为**acs\_newbgpddos**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|活跃连接数|Count|Active\_connection|userId、InstanceId、ip|Maximum|
|高防IP回源流量|bit/s|Back\_Traffic|userId、InstanceId、ip|Maximum|
|高防IP入流量|bit/s|In\_Traffic|userId、InstanceId、ip|Maximum|
|非活跃连接数|Count|Inactive\_connection|userId、InstanceId、ip|Maximum|
|新建连接数|Count|New\_connection|userId、InstanceId、ip|Maximum|
|高防IP出流量|bit/s|Out\_Traffic|userId、InstanceId、ip|Maximum|

