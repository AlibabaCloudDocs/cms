# 智能接入网关（App）

通过本文您可以了解智能接入网关SAG的监控项。

-   **Namespace**为**acs\_smartag**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|SAG实例入向流量|byte|app\_instance\_rx\_data|userId、instanceid|Sum|
|SAG实例入向流量|byte|app\_instance\_rx\_data\_h|userId、instanceid|Sum|
|SAG实例入向限速丢包|PPM|app\_instance\_rx\_drop|userId、instanceId|Value|
|SAG实例入向速率|bit/s|app\_instance\_rx\_rate|userId、instanceId|Average|
|SAG实例出向流量|byte|app\_instance\_tx\_data|userId、instanceId|Sum|
|SAG实例出向流量|byte|app\_instance\_tx\_data\_h|userId、instanceId|Sum|
|SAG实例出向限速丢包|PPM|app\_instance\_tx\_drop|userId、instanceId|Value|
|SAG实例出向速率|bit/s|app\_instance\_tx\_rate|userId、instanceId|Average|
|SAG用户账号入向流量|byte|app\_user\_rx\_data|userId、instanceId、user\_name|Sum|
|SAG用户账号入向流量|byte|app\_user\_rx\_data\_h|userId、instanceId、user\_name|Sum|
|SAG用户账号入向限速丢包|PPM|app\_user\_rx\_drop|userId、instanceId、user\_name|Value|
|SAG用户入向速率|bit/s|app\_user\_rx\_rate|userId、instanceId、user\_name|Average|
|SAG用户账号出向流量|byte|app\_user\_tx\_data|userId、instanceId、user\_name|Sum|
|SAG用户账号出向流量|byte|app\_user\_tx\_data\_h|userId、instanceId、user\_name|Sum|
|SAG用户账号出向限速丢包|PPM|app\_user\_tx\_drop|userId、instanceId、user\_name|Value|
|SAG用户出向速率|bit/s|app\_user\_tx\_rate|userId、instanceId、user\_name|Average|

