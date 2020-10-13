# Serverless工作流

通过本文您可以了解Serverless工作流的监控项。

-   **Namespace**为**acs\_hbaseserverless**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|流程执行时长|Ms|ExecutionExecTimeMs|userId、flowName|Value|
|流程执行失败次数|Count|ExecutionsFailed|userId、flowName|Count|
|流程启动次数|Count|ExecutionsStarted|userId、flowName|Count|
|流程执行停止次数|Count|ExecutionsStopped|userId、flowName|Count|
|流程执行成功次数|Count|ExecutionsSucceeded|userId、flowName|Count|
|流程执行超时次数|Count|ExecutionsTimedOut|userId、flowName|Count|
|流程状态转换数|Count|StepTransitions|userId、flowName|Count|

