# Overview

Custom monitoring allows you to customize metrics as required. You can call the PutCustomMetric API operation to report business metrics about which you are concerned to CloudMonitor for centralized monitoring.

## Limits

The feature of reporting monitoring data has the following limits:

-   The maximum queries per second \(QPS\) is 200 in the China \(Beijing\), China \(Shanghai\), and China \(Hangzhou\) regions, 100 in the China \(Zhangjiakou\) and China \(Shenzhen\) regions, and 50 in all other regions.
-   A maximum of 100 data entries can be reported at a time. The body size of a data entry cannot exceed 256 KB.
-   The value of the `metricName` parameter can only contain letters, digits, and underscores \(\_\). The value must start with a letter. If the first character is not a letter, this character is replaced with an uppercase A. Invalid characters are replaced with underscores \(\_\).
-   The value of the `dimensions` parameter cannot contain equal signs \(=\), ampersands \(&\), or commas \(,\). Invalid characters are replaced with underscores \(\_\).
-   The value of the `metricName` parameter and the key-value pairs of the `dimensions` parameter can be up to 64 bytes in length. Excessive characters are truncated.
-   You need to pay for reporting raw data. You can set the request parameter Type to 1 to report aggregate data free of charge.

## Aggregation methods

After you report raw data by using the PutCustomMetric API operation, CloudMonitor uses the aggregation methods described in the following table to calculate the statistics at 1-minute and 5-minute intervals.

|Aggregation method|Description|
|------------------|-----------|
|Average|Calculates the average value.|
|Maximum|Selects the maximum value.|
|Minimum|Selects the minimum value.|
|Sum|Calculates the total value.|
|SampleCount|Counts the number.|
|SumPerSecond|Calculates the total value divided by the total number of seconds of the aggregation period. You can also calculate the moving average.|
|CountPerSecond|Calculates the count divided by the total number of seconds of the aggregation period. You can also calculate the moving average.|
|LastValue|Selects the last sample value in the aggregation period.|
|P10|Calculates the value of the 10th percentile. This value is greater than 10% of all data in the aggregation period.|
|P20|Calculates the value of the 20th percentile. This value is greater than 20% of all data in the aggregation period.|
|P30|Calculates the value of the 30th percentile. This value is greater than 30% of all data in the aggregation period.|
|P40|Calculates the value of the 40th percentile. This value is greater than 40% of all data in the aggregation period.|
|P50|Calculates the value of the 50th percentile. This value is a median value and greater than 50% of all data in the aggregation period.|
|P60|Calculates the value of the 60th percentile. This value is greater than 60% of all data in the aggregation period.|
|P70|Calculates the value of the 70th percentile. This value is greater than 70% of all data in the aggregation period.|
|P75|Calculates the value of the 75th percentile. This value is greater than 75% of all data in the aggregation period.|
|P80|Calculates the value of the 80th percentile. This value is greater than 80% of all data in the aggregation period.|
|P90|Calculates the value of the 90th percentile. This value is greater than 90% of all data in the aggregation period.|
|P95|Calculates the value of the 95th percentile. This value is greater than 95% of all data in the aggregation period.|
|P98|Calculates the value of the 98th percentile. This value is greater than 98% of all data in the aggregation period.|
|P99|Calculates the value of the 99th percentile. This value is greater than 99% of all data in the aggregation period.|

## Report methods

CloudMonitor provides you with the following methods to report monitoring data:

-   [Report monitoring data by using Cloud Monitor SDK for Java \(Recommended\)](/intl.en-US/Custom monitoring/Report monitoring data/Report monitoring data by using Cloud Monitor SDK for Java (Recommended).md)
-   [Report monitoring data by sending an HTTP request](/intl.en-US/Custom monitoring/Report monitoring data/Report monitoring data by sending an HTTP request.md)
-   [Report monitoring data by using Alibaba Cloud CLI](/intl.en-US/Custom monitoring/Report monitoring data/Report monitoring data by using Alibaba Cloud CLI.md)

