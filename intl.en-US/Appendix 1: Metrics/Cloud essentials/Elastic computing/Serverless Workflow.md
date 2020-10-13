# Serverless Workflow

This topic describes the metrics for Serverless Workflow.

-   Set the **Namespace** parameter to **acs\_hbaseserverless**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|ExecutionExecTimeMs|Ms|ExecutionExecTimeMs|userId and flowName|Value|
|ExecutionsFailed|Count|ExecutionsFailed|userId and flowName|Count|
|ExecutionsStarted|Count|ExecutionsStarted|userId and flowName|Count|
|ExecutionsStopped|Count|ExecutionsStopped|userId and flowName|Count|
|ExecutionsSucceeded|Count|ExecutionsSucceeded|userId and flowName|Count|
|ExecutionsTimedOut|Count|ExecutionsTimedOut|userId and flowName|Count|
|StepTransitions|Count|StepTransitions|userId and flowName|Count|

