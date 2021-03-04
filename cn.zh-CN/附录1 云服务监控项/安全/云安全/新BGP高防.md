# 新BGP高防

通过本文您可以了解DDoS高防的新BGP的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_newbgpddos**。
-   **Period**默认为60秒，也可以为60的整数倍。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|活跃连接数|Count|Active\_connection|userId、InstanceId、ip|Maximum|
|高防IP攻击流量|bit/s|AttackTraffic|userId、InstanceId、ip|Maximum|
|高防IP回源流量|bit/s|Back\_Traffic|userId、InstanceId、ip|Maximum|
|高防IP入流量|bit/s|In\_Traffic|userId、InstanceId、ip|Maximum|
|非活跃连接数|Count|Inactive\_connection|userId、InstanceId、ip|Maximum|
|新建连接数|Count|New\_connection|userId、InstanceId、ip|Maximum|
|高防IP出流量|bit/s|Out\_Traffic|userId、InstanceId、ip|Maximum|
|QPS|CountS|qps|userId、InstanceId、domain|Maximum|
|QPS环比下降率|%|qps\_ratio\_down|userId、InstanceId、domain|Maximum|
|QPS环比增长率|%|qps\_ratio\_up|userId、InstanceId、domain|Maximum|
|2XX状态码|Count|resp2xx|userId、InstanceId、domain|Maximum|
|2XX状态码占比|%|resp2xx\_ratio|userId、InstanceId、domain|Maximum|
|3XX状态码|Count|resp3xx|userId、InstanceId、domain|Maximum|
|3XX状态码占比|%|resp3xx\_ratio|userId、InstanceId、domain|Maximum|
|404状态码|Count|resp404|userId、InstanceId、domain|Maximum|
|404状态码占比|%|resp404\_ratio|userId、InstanceId、domain|Maximum|
|4XX状态码|Count|resp4xx|userId、InstanceId、domain|Maximum|
|4XX状态码占比|%|resp4xx\_ratio|userId、InstanceId、domain|Maximum|
|5XX状态码|Count|resp5xx|userId、InstanceId、domain|Maximum|
|5XX状态码占比|%|resp5xx\_ratio|userId、InstanceId、domain|Maximum|
|2XX回源状态码|Count|upstream\_resp2xx|userId、InstanceId、domain|Maximum|
|2XX回源状态码占比|%|upstream\_resp2xx\_ratio|userId、InstanceId、domain|Maximum|
|3XX回源状态码|Count|upstream\_resp3xx|userId、InstanceId、domain|Maximum|
|3XX回源状态码占比|%|upstream\_resp3xx\_ratio|userId、InstanceId、domain|Maximum|
|404回源状态码|Count|upstream\_resp404|userId、InstanceId、domain|Maximum|
|404回源状态码占比|%|upstream\_resp404\_ratio|userId、InstanceId、domain|Maximum|
|4XX回源状态码|Count|upstream\_resp4xx|userId、InstanceId、domain|Maximum|
|4XX回源状态码占比|%|upstream\_resp4xx\_ratio|userId、InstanceId、domain|Maximum|
|5XX回源状态码|Count|upstream\_resp5xx|userId、InstanceId、domain|Maximum|
|5XX回源状态码占比|%|upstream\_resp5xx\_ratio|userId、InstanceId、domain|Maximum|

