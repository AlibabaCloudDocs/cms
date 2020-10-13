# ApsaraDB for MongoDB-Single Node Instance

This topic describes the metrics for standalone ApsaraDB for MongoDB instances.

-   Set the **Namespace** parameter to **acs\_mongodb**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|\(Single node\) SingleNodeCPUUtilization|%|SingleNodeCPUUtilization|userId and instanceId|Average|
|\(Single node\) SingleNodeConnectionAmount|Count|SingleNodeConnectionAmount|userId and instanceId|Average|
|\(Single node\) SingleNodeConnectionUtilization|%|SingleNodeConnectionUtilization|userId and instanceId|Average|
|\(Single node\) SingleNodeDataDiskAmount|Byte|SingleNodeDateDiskAmount|userId and instanceId|Average|
|\(Single node\) SingleNodeDiskUtilization|%|SingleNodediskUtilization|userId and instanceId|Average|
|\(Single node\) SingleNodeIntranetIn|Byte|SingleNodeIntranetIn|userId and instanceId|Average|
|\(Single node\) SingleNodeIntranetOut|Byte|SingleNodeIntranetIn|userId and instanceId|Average|
|\(Single node\) SingleNodeMemoryUtilization|%|SingleNodeMemoryUtilization|userId and instanceId|Average|
|\(Single node\) SingleNodeNumberRequests|Count|SingleNodeNumberRequests|userId and instanceId|Average|
|\(Single node\) SingleNodeOpCommand|Count|SingleNodeOpCommand|userId and instanceId|Average|
|\(Single node\) SingleNodeOpDelete|Count|SingleNodeOpDelete|userId and instanceId|Average|
|\(Single node\) SingleNodeOpGetmore|Count|SingleNodeOPGetmore|userId and instanceId|Average|
|\(Single node\) SingleNodeOpInsert|Count|SingleNodeOpInsert|userId and instanceId|Average|
|\(Single node\) SingleNodeOpQuery|Count|SingleNodeOpQuery|userId and instanceId|Average|
|\(Single node\) SingleNodeOpUpdate|Count|SingleNodeOpUpdate|userId and instanceId|Average|
|\(Single node\) SingleNodeQPS|Count|SingleNodeQPS|userId and instanceId|Average|

