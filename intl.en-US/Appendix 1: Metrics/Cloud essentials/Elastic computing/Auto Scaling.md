# Auto Scaling

This topic describes the metrics for Auto Scaling.

-   Set the **Namespace** parameter to **acs\_ess\_dashboard**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|Maximum Instance Number|Count|MaxInstanceCount|userId and instanceId|Average, Minimum, and Maximum|
|Minimum Instance Number|Count|MinInstanceCount|userId and instanceId|Average, Minimum, and Maximum|
|Number of instances being removed|Count|PendingInstanceCount|userId and instanceId|Average, Minimum, and Maximum|
|Number of instances being added|Count|RemovingInstanceCount|userId and instanceId|Average, Minimum, and Maximum|
|Removing Instance Number|Count|RunningInstanceCount|userId and instanceId|Average, Minimum, and Maximum|
|Instance Number|Count|TotalInstanceCount|userId and instanceId|Average, Minimum, and Maximum|

