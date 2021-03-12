# PolarDB

This topic describes the metrics for ApsaraDB for PolarDB.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_polardb**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|Connection Utilization|%|instance\_connection\_utilization|userId and instanceId|Maximum, Minimum, and Average|
|CPUUtilization|%|instance\_cpu\_utilization|userId and instanceId|Average|
|Input Bandwidth|bit/s|instance\_input\_bandwidth|userId and instanceId|Average|
|Memory Utilization|%|instance\_memory\_utilization|userId and instanceId|Average|
|Output Banwidth|bit/s|instance\_output\_bandwidth|userId and instanceId|Average|

