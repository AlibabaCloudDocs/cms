# Openad

This topic describes the metrics for Open Ad.

-   Set the **Namespace** parameter to **acs\_openad**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|\(DSP\)RTB PV|count|bid\_pv|userId and dspId|Sum|
|\(DSP\)RTB QPS|count/s|bid\_qps|userId and dspId|Value|
|\(DSP\)Ad Click PV|count|click\_pv|userId and dspId|Sum|
|\(DSP\)Ad Click QPS|count/s|click\_qps|userId and dspId|Value|
|\(DSP\)Ad Click Delay|ms|click\_rt|userId and dspId|Value|
|\(DSP\)dmp\_crowd\_num|count/day|dmp\_crowd\_num|userId and dspId|Value|
|\(DSP\)dmp\_crowd\_pv|count/day|dmp\_crowd\_pv|userId and dspId|Value|
|\(DSP\)dmp\_storage|byte/day|dmp\_storage|userId and dspId|Value|
|\(DSP\)Ad Impression PV|count|show\_pv|userId and dspId|Sum|
|\(DSP\)Ad Impression QPS|count/s|show\_qps|userId and dspId|Value|
|\(DSP\)Ad Impression Delay|ms|show\_rt|userId and dspId|Value|
|\(SSP\)RTB PV|count|ssp\_bid\_pv|userId and sspId|Sum|
|\(SSP\)RTB QPS|count/s|ssp\_bid\_qps|userId and sspId|Value|
|\(SSP\)Ad Click PV|count|ssp\_click\_pv|userId and sspId|Sum|
|\(SSP\)Ad Click QPS|count/s|ssp\_click\_qps|userId and sspId|Value|
|\(SSP\)Ad Click delay|ms|ssp\_click\_rt|userId and sspId|Value|
|\(SSP\)DMS Crowd Number|count/day|ssp\_dmp\_crowd\_num|userId and sspId|Value|
|\(SSP\)DMS Crowd PV|count/day|ssp\_dmp\_crowd\_pv|userId and sspId|Value|
|\(SSP\)Ad Impression PV|count|ssp\_show\_pv|userId and sspId|Sum|
|\(SSP\)AAd Impression QPS|count/s|ssp\_show\_qps|userId and sspId|Value|
|\(SSP\)Ad Impression delay|ms|ssp\_show\_rt|userId and sspId|Value|
|umeng\_crowd\_num|count/day|umeng\_crowd\_num|userId and dspId|Value|
|umeng\_crowd\_pv|count/day|umeng\_crowd\_pv|userId and dspId|Value|

