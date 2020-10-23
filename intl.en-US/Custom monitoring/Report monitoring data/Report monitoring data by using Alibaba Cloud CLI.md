# Report monitoring data by using Alibaba Cloud CLI

This topic describes how to report monitoring data by using Alibaba Cloud Command Line Interface \(CLI\).

## Grant permissions on Cloud Monitor to a RAM user

Cloud Monitor allows you to use an Alibaba Cloud account or a Resource Access Management \(RAM\) user to report monitoring data. If a RAM user needs to use an AccessKey pair to report monitoring data, you must grant permissions on Cloud Monitor to the RAM user by performing the following steps:

1.  Log on to the [RAM console](https://ram.console.aliyun.com/) with an Alibaba Cloud account.
2.  Create a RAM user.

    For more information, see [Create a RAM user](/intl.en-US/RAM User Management/Create a RAM user.md).

3.  Create an AccessKey pair for the RAM user.

    For more information, see [Create an AccessKey pair for a RAM user](/intl.en-US/Security Settings/AccessKey pairs/Create an AccessKey pair for a RAM user.md).

4.  Attach the AliyunCloudMonitorFullAccess policy to the RAM user.

    For more information, see [Grant permissions to a RAM user](/intl.en-US/RAM User Management/Grant permissions to a RAM user.md).


## Install and configure Alibaba Cloud CLI

For more information, see [Install Alibaba Cloud CLI in Windows](https://www.alibabacloud.com/help/doc-detail/121510.htm) or [Install Alibaba Cloud CLI in Linux](https://www.alibabacloud.com/help/doc-detail/121541.htm).

## Report monitoring data

Call the PutCustomMetric API operation to report monitoring data. For more information, see [PutCustomMetric](/intl.en-US/API Reference/Custom monitoring/PutCustomMetric.md).

Sample command:

```
aliyun cms PutCustomMetric  --MetricList.1.MetricName cpu_total --MetricList.1.Dimensions '{"sampleName1":"value1","sampleName2":"value2"}' --MetricList.1.Time 1555390981421 --MetricList.1.Type 0 --MetricList.1.Period 60 --MetricList.1.Values '{"value":10.5}' --MetricList.1.GroupId "0"
```

Cloud Monitor returns the status code 200, indicating that the monitoring data is reported.

```
{
  "Message": "success",
  "RequestId": "F69F5623-DDD6-42AE-AE59-87A2B841620B",
  "Code": "200"
}
```

## Status codes

The following table describes the status codes that Cloud Monitor may return when you report monitoring data by using Alibaba Cloud CLI.

|Status code|Description|
|:----------|:----------|
|200|The status code returned when the monitoring data is reported.|
|206|-   If the error message is `''reach Max time series num''`, you used up the time series quota. We recommend that you purchase a higher quota or remove unnecessary time series.
-   If the error message is `''not allowed original value, please upgrade service''`, you use a free edition of Cloud Monitor to which you cannot report raw data.
-   If the error message is `''type is invalid''`, the value of the Type parameter is invalid. Make sure that the value of this parameter is 0 or 1. |
|400|The error code returned because the request contains a syntax error.|
|403|The error code returned because the verification fails, the rate reaches the throttling threshold, or the required permission is unavailable.|
|500|The error code returned because an internal server error occurred.|

