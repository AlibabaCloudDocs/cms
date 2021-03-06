# ApsaraDB for POLARDB PostgreSQL/Oracle

This topic describes the metrics of PolarDB for PostgreSQL or Oracle.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_polardb**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|Active Connection|Count|active\_connections|userId, clusterId, and instanceId|Average|
|BlockRead|Count|blks\_read\_delta|userId, clusterId, and instanceId|Value|
|Connection Usage|%|conn\_usage|userId, clusterId, and instanceId|Average|
|CPU Usage|%|cpu\_total|userId, clusterId, and instanceId|Average|
|DB Age|xids|db\_age|userId, clusterId, and instanceId|Average|
|Memory Usage|%|mem\_usage|userId, clusterId, and instanceId|Average|
|Data Size|Mbyte|pls\_data\_size|userId, clusterId, and instanceId|Value|
|IOPS|Frequency|pls\_iops|userId, clusterId, and instanceId|Average|
|Read IOPS|Frequency|pls\_iops\_read|userId, clusterId, and instanceId|Average|
|Write IOPS|Frequency|pls\_iops\_write|userId, clusterId, and instanceId|Average|
|WAL Log Size|Mbyte|pls\_pg\_wal\_dir\_size|userId, clusterId, and instanceId|Value|
|IO Throughout|Mbyte/s|pls\_throughput|userId, clusterId, and instanceId|Average|
|Read IO Throughput|Mbyte/s|pls\_throughput\_read|userId, clusterId, and instanceId|Average|
|Write IO Throughput|Mbyte/s|pls\_throughput\_write|userId, clusterId, and instanceId|Average|
|Swell Time|s|swell\_time|userId, clusterId, and instanceId|Average|
|TPS|Frequency|tps|userId, clusterId, and instanceId|Average|
|Rollback Ratio|%|rollback\_ratio|userId, clusterId, and instanceId|userId, clusterId, and instanceId|

