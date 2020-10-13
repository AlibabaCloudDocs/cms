# Log Service

This topic describes the metrics for Log Service.

-   Set the **Namespace** parameter to **acs\_sls\_dashboard**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|Number of error IPs|Frequency|AlarmIPCount|userId, project, logstore, alarm\_type, and source\_ip|Count|
|Number of errors|Frequency|AlarmPV|userId, project, and logstore|Sum|
|Number of error instances|Frequency|AlarmUV|userId, project, and logstore|Count|
|Delay Time of Consumption|Second|ConsumerGroupFailBehind|userId, project, logstore, and consumerGroup|Maximum|
|Lines failed to be resolved|Lines|FailedLines|userId, project, and logstore|Sum|
|Lines|Lines/Minute|InflowLine|userId, project, and logstore|Sum|
|Service Status|Count|LogCodeQPS|userId, project, logstore, and status|Count|
|Write Traffic|Byte|LogInflow|userId, project, and logstore|Sum|
|Number of operations|Count|LogMethodQPS|userId, project, logstore, and method|Count|
|Read Traffic|Byte|LogOutflow|userId, project, and logstore|Sum|
|Size of Raw Data|Byte|NetFlow|userId, project, and logstore|Sum|
|Traffic resolved successfully|Byte|SuccessdByte|userId, project, and logstore|Sum|
|Lines resolved successfully|Lines|SuccessdLines|userId, project, and logstore|Sum|
|Overall QPS|Count|SumQPS|userId, project, and logstore|Count|

