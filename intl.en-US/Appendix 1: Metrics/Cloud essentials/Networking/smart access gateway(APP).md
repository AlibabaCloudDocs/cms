# smart access gateway\(APP\)

This topic describes the metrics for Smart Access Gateway.

-   Set the **Namespace** parameter to **acs\_smartag**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|app\_instance\_rx\_data|byte|app\_instance\_rx\_data|userId and instanceId|Sum|
|app\_instance\_rx\_data\_hour|byte|app\_instance\_rx\_data\_h|userId and instanceId|Sum|
|app\_instance\_rx\_drop|packet/min|app\_instance\_rx\_drop|userId and instanceId|Value|
|app\_instance\_rx\_rate|bit/s|app\_instance\_rx\_rate|userId and instanceId|Average|
|app\_instance\_tx\_data|byte|app\_instance\_tx\_data|userId and instanceId|Sum|
|app\_instance\_tx\_data\_hour|byte|app\_instance\_tx\_data\_h|userId and instanceId|Sum|
|app\_instance\_tx\_drop|packet/min|app\_instance\_tx\_drop|userId and instanceId|Value|
|app\_instance\_tx\_rate|bit/s|app\_instance\_tx\_rate|userId and instanceId|Average|
|app\_user\_rx\_data|byte|app\_user\_rx\_data|userId, instanceId, and user\_name|Sum|
|app\_user\_rx\_data\_hour|byte|app\_user\_rx\_data\_h|userId, instanceId, and user\_name|Sum|
|app\_user\_rx\_drop|packet/min|app\_user\_rx\_drop|userId, instanceId, and user\_name|Value|
|app\_user\_rx\_rate|bit/s|app\_user\_rx\_rate|userId, instanceId, and user\_name|Average|
|app\_user\_tx\_data|byte|app\_user\_tx\_data|userId, instanceId, and user\_name|Sum|
|app\_user\_tx\_data\_hour|byte|app\_user\_tx\_data\_h|userId, instanceId, and user\_name|Sum|
|app\_user\_tx\_drop|packet/min|app\_user\_tx\_drop|userId, instanceId, and user\_name|Value|
|app\_user\_tx\_rate|bit/s|app\_user\_tx\_rate|userId, instanceId, and user\_name|Average|

