# ApsaraVideo for Media Processing

This topic describes the metrics for ApsaraVideo for Media Processing.

-   Set the **Namespace** parameter to **acs\_mps**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|RequestSuccessRate|%|RequestSuccessRate|userId|Value|
|SnapshotTasks|Count/Min|SnapshotTasks|userId and pipelineId|Value|
|TranscodingDuration|s|TranscodingDuration|userId and pipelineId|Value|
|TranscodingTasks|Count/Min|TranscodingTasks|userId and pipelineId|Value|

