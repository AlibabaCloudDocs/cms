# AIRec

This topic describes the metrics for Artificial Intelligence Recommendation.

-   Set the **Namespace** parameter to **acs\_airec**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|BehaviorFailedTps|Count/Second|BehaviorFailedTps|userId and instanceId|Sum|
|BehaviorTimeLag|second|BehaviorTimeLag|userId and instanceId|Average|
|BehaviorTps|Count/Second|BehaviorTps|userId and instanceId|Sum|
|ItemFailedTps|Count/Second|ItemFailedTps|userId and instanceId|Sum|
|ItemQuotaUsedRatio|Percent|ItemQuotaUsedRatio|userId and instanceId|Average|
|ItemTpsOverRate|Count/Second|ItemTps|userId and instanceId|Sum|
|QPS|Count/Second|OverRateQPS|userId and instanceId|Count|
|RecommendLatency|ms|RecommendLatency|userId and instanceId|Average|
|RecommendQPS|Count/Second|RecommendQPS|userId and instanceId|Count|
|UserFailedTps|Count/Second|UserFailedTps|userId and instanceId|Sum|
|UserQuotaUsedRatio|Percent|UserQuotaUsedRatio|userId and instanceId|Average|
|UserTps|Count/Second|UserTps|userId and instanceId|Sum|

