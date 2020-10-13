# PAI-EAS inference service

This topic describes the metrics for the Elastic Algorithm Service \(EAS\) provided by Machine Learning Platform for AI \(PAI\) for online inference.

-   Set the **Namespace** parameter to **acs\_learn**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|CPUConsumption|count|cpu\_core\_usage|userId and serviceName|Average and Maximum|
|GPUUtilization|%|gpu\_util|userId and serviceName|Average and Maximum|
|MemoryComsumption|byte|memory\_rss|userId and serviceName|Average, Maximum, and Minimum|
|QueryPerSecondTotal|frequency|qps\_total|userId and serviceName|Value, Average, and Maximum|
|ResponsePerSecondWithStatusCode2xx|frequency|rps\_status\_2xx|userId and serviceName|Average, Maximum, Value, and Minimum|
|2xxResponseRatio|%|rps\_status\_2xx\_ratio|userId and serviceName|Average, Minimum, Maximum, and Value|
|ResponsePerSecondWithStatusCode4xx|frequency|rps\_status\_4xx|userId and instanceId|Average, Maximum, and Value|
|4xxResponseRatio|%|rps\_status\_4xx\_ratio|userId and serviceName|Average, Maximum, Minimum, and Value|
|ResponsePerSecondWithStatusCode5xx|frequency|rps\_status\_5xx|userId and serviceName|Average, Maximum, and Value|
|5xxResponseRatio|%|rps\_status\_5xx\_ratio|userId and serviceName|Average, Maximum, Minimum, and Value|
|ResponseTime|microseconds|rt|userId and serviceName|Average, Maximum, and Minimum|
|IngressTraffic|bps|traffic\_in|userId and serviceName|Average, Maximum, Minimum, and Value|
|EgressTraffic|bps|traffic\_out|userId and serviceName|Average, Maximum, Minimum, and Value|

