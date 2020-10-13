# AnalyticDB for mysql 3.0

This topic describes the metrics for AnalyticDB for MySQL 3.0.

-   Set the **Namespace** parameter to **acs\_adb**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|Connections|Count|connctions|userId and instanceId|Average|
|DiskUsedPercent|%|disk\_used\_percent|userId and instanceId|Average|
|InsertAvgRt|Milliseconds|insert\_avg\_rt|userId and instanceId|Average|
|InsertInBytes|Mbyte|insert\_in\_bytes|userId and instanceId|Average|
|InsertMaxRt|Milliseconds|insert\_max\_rt|userId and instanceId|Average|
|QPS|Count|qps|userId and instanceId|Average|
|QueryAvgRt|Milliseconds|query\_avg\_rt|userId and instanceId|Average|
|QueryMaRt|Milliseconds|query\_max\_rt|userId and instanceId|Average|
|QueryTotalWaitTime|Milliseconds|query\_total\_wait\_time|userId and instanceId|Average|
|TPS|Count|tps|userId and instanceId|Average|
|AvgCpuUsed|%|worker\_avg\_cpu\_used|userId and instanceId|Average|
|AvgReadBytes|Mbyte|worker\_avg\_read\_bytes|userId and instanceId|Average|
|AvgReadIOPS|Frequency|worker\_avg\_iops|userId and instanceId|Average|
|AvgWriteBytes|Mbyte|worker\_avg\_bytes|userId and instanceId|Average|
|AvgWriteIOPS|Frequency|worker\_avg\_iops|userId and instanceId|Average|

