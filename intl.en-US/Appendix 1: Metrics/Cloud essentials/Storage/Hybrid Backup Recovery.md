# Hybrid Backup Recovery

This topic describes the metrics for Hybrid Backup Recovery \(HBR\).

-   Set the **Namespace** parameter to **acs\_hbr**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|vault storage size|byte|vault\_storage\_size|userId and vaultId|Maximum|

