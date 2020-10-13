# Apsara File Storage for HDFS

This topic describes the metrics for Apsara File Storage for HDFS.

-   Set the **Namespace** parameter to **acs\_hdfs**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|ReadIOPS|Count/Second|read\_iops|userId and instanceId|Average|
|ReadIOSize|Byte|read\_iosize|userId and instanceId|Average|
|ReadThroughput|Byte/s|read\_throughput|userId and instanceId|Average|
|RemainingStorageSpace|Byte|remaining\_storagespace|userId and instanceId|Average|
|StorageUtilization|%|storageutilization|userId and instanceId|Average|
|UsedStorageSpace|Byte|used\_storagespace|userId and instanceId|Average|
|WriteIOPS|Count/Second|write\_iops|userId and instanceId|Average|
|WriteIOSize|Byte|write\_iosize|userId and instanceId|Average|
|write\_throughput|Byte/s|write\_throughput|userId and instanceId|Average|

