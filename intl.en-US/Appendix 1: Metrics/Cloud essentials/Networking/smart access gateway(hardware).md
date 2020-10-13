# smart access gateway\(hardware\)

This topic describes the metrics for Smart Access Gateway.

-   Set the **Namespace** parameter to **acs\_smartag**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|SagCpuUtilization|%|SagCpuUtilization|userId, instanceId, and box\_sn|Average|
|SagDiskUtilization|%|SagDiskUtilization|userId, instanceId, and box\_sn|Average|
|SagMemoryUtilization|%|SagMemoryUtilization|userId, instanceId, and box\_sn|Average|
|box\_lte\_rx\_drop|packet/min|box\_lte\_rx\_drop|userId, instanceId, and box\_sn|Value|
|lte\_rx\_rate|bit/s|box\_lte\_rx\_rate|userId, instanceId, and box\_sn|Average|
|box\_lte\_tx\_drop|packet/min|box\_lte\_tx\_drop|userId, instanceId, and box\_sn|Value|
|box\_lte\_tx\_rate|bit/s|box\_lte\_tx\_rate|userId, instanceId, and box\_sn|Average|
|box\_wan\_wireless\_rx.rate|bit/s|box\_wan\_wireless\_rx.rate|userId, instanceId, and box\_sn|Average|
|box\_wan\_wireless\_tx.rate|bit/s|box\_wan\_wireless\_tx.rate|userId, instanceId, and box\_sn|Average|
|lte\_rx\_drop|packet/min|lte\_rx\_drop|userId and instanceId|Average|
|lte\_rx\_rate|bit/s|lte\_rx\_rate|userId and instanceId|Average|
|lte\_tx\_drop|packet/min|lte\_tx\_drop|userId and instanceId|Average|
|lte\_tx\_rate|bit/s|lte\_tx\_rate|userId and instanceId|Average|
|rx\_bandwidth utilization|%|rx\_bandwidth\_utilization|userId and instanceId|Average|
|sag\_box\_nqa\_latency|ms|sag\_box\_nqa\_latency|userId and instanceId|Average|
|sag\_box\_nqa\_loss\_data|packet|sag\_box\_nqa\_loss\_data|userId and instanceId|Value|
|sag\_box\_nqa\_loss\_percent|%|sag\_box\_nqa\_loss\_percent|userId and instanceId|Value|
|sag\_box\_wifi\_rx\_bps|bit/s|sag\_box\_wifi\_rx\_bps|userId and instanceId|Average|
|sag\_box\_wifi\_rx\_pps|packet/s|sag\_box\_wifi\_rx\_pps|userId and instanceId|Average|
|sag\_box\_wifi\_tx\_bps|bit/s|sag\_box\_wifi\_tx\_bps|userId and instanceId|Average|
|sag\_box\_wifi\_tx\_pps|packet/s|sag\_box\_wifi\_tx\_pps|userId and instanceId|Average|
|sn\_box\_wifi\_rx\_bps|bit/s|sn\_box\_wifi\_rx\_bps|userId, instanceId, and box\_sn|Average|
|sn\_box\_wifi\_rx\_pps|packet/s|sn\_box\_wifi\_rx\_pps|userId, instanceId, and box\_sn|Average|
|sn\_box\_wifi\_tx\_bps|bit/s|sn\_box\_wifi\_tx\_bps|userId, instanceId, and box\_sn|Average|
|sn\_box\_wifi\_tx\_pps|packet/s|sn\_box\_wifi\_tx\_pps|userId, instanceId, and box\_sn|Average|
|tx\_bandwidth\_utilization|%|tx\_bandwidth\_utilization|userId and instanceId|Average|

