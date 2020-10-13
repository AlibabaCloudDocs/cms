# 云数据库MongoDB版-单节点实例

通过本文您可以了解云数据库MongoDB版的单节点实例的监控项。

-   **Namespace**为**acs\_mongodb**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|（单节点）CPU使用率|%|SingleNodeCPUUtilization|userId、instanceId|Average|
|（单节点）连接数使用量|Count|SingleNodeConnectionAmount|userId、instanceId|Average|
|（单节点）连接数使用率|%|SingleNodeConnectionUtilization|userId、instanceId|Average|
|（单节点）数据占用磁盘空间量|Byte|SingleNodeDateDiskAmount|userId、instanceId|Average|
|（单节点）磁盘使用率|%|SingleNodediskUtilization|userId、instanceId|Average|
|（单节点）网络入流量|Byte|SingleNodeIntranetIn|userId、instanceId|Average|
|（单节点）网络入流量|Byte|SingleNodeIntranetIn|userId、instanceId|Average|
|（单节点）内存使用率|%|SingleNodeMemoryUtilization|userId、instanceId|Average|
|（单节点）请求数|Count|SingleNodeNumberRequests|userId、instanceId|Average|
|（单节点）Command操作次数|Count|SingleNodeOpCommand|userId、instanceId|Average|
|（单节点）Delete操作次数|Count|SingleNodeOpDelete|userId、instanceId|Average|
|（单节点）Getmore操作次数|Count|SingleNodeOPGetmore|userId、instanceId|Average|
|（单节点）Insert操作次数|Count|SingleNodeOpInsert|userId、instanceId|Average|
|（单节点）Query操作次数|Count|SingleNodeOpQuery|userId、instanceId|Average|
|（单节点）Update操作次数|Count|SingleNodeOpUpdate|userId、instanceId|Average|
|（单节点）QPS|Count|SingleNodeQPS|userId、instanceId|Average|

