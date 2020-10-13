# polarDB

This topic describes the metrics for ApsaraDB for POLARDB.

-   Set the **Namespace** parameter to **acs\_polardb**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|Connection Utilization|%|instance\_connection\_utilization|userId and instanceId|Maximum, Minimum, and Average|
|CPUUtilization|%|instance\_cpu\_utilization|userId and instanceId|Average|
|Input Bandwidth|bit/s|instance\_input\_bandwidth|userId and instanceId|Average|
|Memory Utilization|%|instance\_memory\_utilization|userId and instanceId|Average|
|Output Banwidth|bit/s|instance\_output\_bandwidth|userId and instanceId|Average|

