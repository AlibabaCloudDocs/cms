# DCDN

This topic describes the metrics for Dynamic Route for CDN.

-   Set the **Namespace** parameter to **acs\_dcdn**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|Peak Bandwidth|bit/s|BPS|userId and instanceId|Average|
|IPAOrigConnError|%|IPAOrigConnError|userId, domain\_name, isp, and location|Value|
|IPAOrigError|%|IPAOrigError|userId, domain\_name, isp, and location|Value|
|IPAOrigTimeout|%|IPAOrigtimeout|userId, domain\_name, isp, and location|Value|
|QPS|Count|QPS|userId and instanceId|Average|
|bps\_in|bit/s|bps\_in|userId and domain\_name|Maximum|
|bps\_out|bit/s|bps\_out|userId and domain\_name|Maximum|
|4XX Return Code ratio|%|code4xx|userId and instanceId|Average|
|5XX Return Code ratio|%|code5xx|userId and instanceId|Average|
|1xxratio|%|code\_ratio\_1|userId and domain\_name|Maximum|
|2xxratio|%|code\_ratio\_2|userId and domain\_name|Maximum|
|3xxratio|%|code\_ratio\_3|userId and domain\_name|Maximum|
|4xxratio|%|code\_ratio\_4|userId and domain\_name|Maximum|
|5xxratio|%|code\_ratio\_5|userId and domain\_name|Maximum|
|qps|countSecond|dcdn\_qps|userId and domain\_name|Maximum|
|domain\_count|count|domain\_count|userId, isp, and location|Sum|
|edge\_fftb|milliseconds|edge\_fftb|userId, domain\_name, isp, and location|Maximum|
|Hit Rate|%|hitRate|userId and instanceId|Average|
|hit\_rate|%|hit\_rate|userId and domain\_name|Maximum|
|ipa\_conn|count|ipa\_conn|userId, domain\_name, isp, and location|Maximum|
|ipa\_edge\_bps|bit/s|ipa\_edge\_bps|userId, domain\_name, isp, and location|Maximum|
|ipa\_new\_conn|count|ipa\_new\_conn|userId, domain\_name, isp, and location|Maximum|
|ipa\_ori\_bps|bit/s|ipa\_ori\_bps|userId, domain\_name, isp, and location|Maximum|
|ori\_fftb|milliseconds|ori\_fftb|userId, domain\_name, isp, and location|Maximum|
|rt|milliseconds|rt|userId and domain\_name|Maximum|

