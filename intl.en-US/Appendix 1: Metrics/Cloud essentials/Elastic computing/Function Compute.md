# Function Compute

This topic describes the metrics for Function Compute.

-   Set the **Namespace** parameter to **acs\_fc**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|FunctionAvgDuration|ms|FunctionAvgDuration|userId, region, serviceName, and functionName|Value|
|FunctionBillableInvocations|count|FunctionBillableInvocations|userId, region, serviceName, and functionName|Value|
|FunctionBillableInvocationsRate|%|FunctionBillableInvocationsRate|userId, region, serviceName, and functionName|Value|
|FunctionClientErrors|count|FunctionClientErrors|userId, region, serviceName, and functionName|Value|
|FunctionClientErrorsRate|%|FunctionClientErrorsRate|userId, region, serviceName, and functionName|Value|
|FunctionErrors|count|FunctionFunctionErrors|userId, region, serviceName, and functionName|Value|
|FunctionErrorsRate|%|FunctionFunctionErrorsRate|userId, region, serviceName, and functionName|Value|
|FunctionMaxMemoryUsage|MB|FunctionMaxMemoryUsage|userId, region, serviceName, and functionName|Value|
|FunctionServerErrors|count|FunctionServerErrors|userId, region, serviceName, and functionName|Value|
|ServerErrorsRate|%|FunctionServerErrorsRate|userId, region, serviceName, and functionName|Value|
|Throttles|count|FuntionThrottles|userId, region, serviceName, and functionName|Value|
|ThrottlesRate|%|FuntionThrottlesRate|userId, region, serviceName, and functionName|Value|
|TotalInvocations|count|FuntionTotalInvocations|userId, region, serviceName, and functionName|Value|
|RegionBillableInvocations|count|RegionBillableInvocations|userId and region|Value|
|RegionbillableInvocationsRate|%|RegionbillableInvocationsRate|userId and region|Value|
|RegionClientErrors|count|RegionClientErrors|userId and region|Value|
|RegionClientErrorsRate|%|RegionClientErrorsRate|userId and region|Value|
|RegionServerErrorsRate|%|RegionServerErrors|userId and region|Value|
|RegionThrottles|count|RegionThrottles|userId and region|Value|
|RegionThrttlesRate|%|RegionThrttlesRate|userId and region|Value|
|RegionTotalInvocations|count|RegionTotalInvocations|userId and region|Value|
|ServiceBillableInvocations|count|ServiceBillableInvocations|userId, region, and serviceName|Value|
|ServiceBillableInvocationsRate|%|ServiceBillableInvocationsRate|userId, region, and serviceName|Value|
|ServiceClientErrors|count|ServiceClientErrors|userId, region, and serviceName|Value|
|ServiceClientErrorsRate|%|ServiceClientErrorsRate|userId, region, and serviceName|Value|
|ServiceServerErrors|count|ServiceServerErrors|userId, region, and serviceName|Value|
|ServiceServerErrorsRate|%|ServiceServerErrorsRate|userId, region, and serviceName|Value|
|ServiceThrottles|count|ServiceThrottles|userId, region, and serviceName|Value|
|ServiceThrottlesRate|%|ServiceThrottlesRate|userId, region, and serviceName|Value|
|ServiceTotalInvocations|count|ServiceTotalInvocations|userId, region, and serviceName|Value|

