# Function Compute

This topic describes the metrics for Function Compute.

-   Set the **Namespace** parameter to **acs\_fc**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|FunctionAvgDuration|ms|FunctionAvgDuration|userId, region, serviceName, and functionName|Value|
|FunctionBillableInvocations|Count|FunctionBillableInvocations|userId, region, serviceName, and functionName|Value|
|FunctionBillableInvocationsRate|%|FunctionBillableInvocationsRate|userId, region, serviceName, and functionName|Value|
|FunctionClientErrors|Count|FunctionClientErrors|userId, region, serviceName, and functionName|Value|
|FunctionClientErrorsRate|%|FunctionClientErrorsRate|userId, region, serviceName, and functionName|Value|
|FunctionErrors|Count|FunctionFunctionErrors|userId, region, serviceName, and functionName|Value|
|FunctionErrorsRate|%|FunctionFunctionErrorsRate|userId, region, serviceName, and functionName|Value|
|FunctionMaxMemoryUsage|MB|FunctionMaxMemoryUsage|userId, region, serviceName, and functionName|Value|
|FunctionServerErrors|Count|FunctionServerErrors|userId, region, serviceName, and functionName|Value|
|FunctionServerErrorsRate|%|FunctionServerErrorsRate|userId, region, serviceName, and functionName|Value|
|FunctionThrottles|Count|FunctionThrottles|userId, region, serviceName, and functionName|Value|
|FunctionThrottlesRate|%|FunctionThrottlesRate|userId, region, serviceName, and functionName|Value|
|FunctionTotalInvocations|Count|FunctionTotalInvocations|userId, region, serviceName, and functionName|Value|
|RegionBillableInvocations|Count|RegionBillableInvocations|userId and region|Value|
|RegionbillableInvocationsRate|%|RegionbillableInvocationsRate|userId and region|Value|
|RegionClientErrors|Count|RegionClientErrors|userId and region|Value|
|RegionClientErrorsRate|%|RegionClientErrorsRate|userId and region|Value|
|RegionServerErrors|%|RegionServerErrors|userId and region|Value|
|RegionThrottles|Count|RegionThrottles|userId and region|Value|
|RegionThrttlesRate|%|RegionThrttlesRate|userId and region|Value|
|RegionTotalInvocations|Count|RegionTotalInvocations|userId and region|Value|
|ServiceBillableInvocations|Count|ServiceBillableInvocations|userId, region, and serviceName|Value|
|ServiceBillableInvocationsRate|%|ServiceBillableInvocationsRate|userId, region, and serviceName|Value|
|ServiceClientErrors|Count|ServiceClientErrors|userId, region, and serviceName|Value|
|ServiceClientErrorsRate|%|ServiceClientErrorsRate|userId, region, and serviceName|Value|
|ServiceServerErrors|Count|ServiceServerErrors|userId, region, and serviceName|Value|
|ServiceServerErrorsRate|%|ServiceServerErrorsRate|userId, region, and serviceName|Value|
|ServiceThrottles|Count|ServiceThrottles|userId, region, and serviceName|Value|
|ServiceThrottlesRate|%|ServiceThrottlesRate|userId, region, and serviceName|Value|
|ServiceTotalInvocations|Count|ServiceTotalInvocations|userId, region, and serviceName|Value|

