# DescribeSiteMonitorQuota

Queries the quotas and version of site monitoring.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeSiteMonitorQuota&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeSiteMonitorQuota|The operation that you want to perform. Set the value to DescribeSiteMonitorQuota. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Data|Struct|N/A|The quotas and version of site monitoring. |
|SecondMonitor|Boolean|false|Indicates whether the second-level monitoring is enabled. Valid values:

-   true
-   false |
|SiteMonitorIdcQuota|Integer|5|The quota of detection points that are provided by Alibaba Cloud. Five detection points are provided for free. |
|SiteMonitorOperatorQuotaQuota|Integer|0|The quota of detection points that are not provided by Alibaba Cloud. Default value: 0. |
|SiteMonitorQuotaTaskUsed|Integer|6|The used quota of site monitoring tasks. |
|SiteMonitorTaskQuota|Integer|10|The quota of site monitoring tasks. |
|SiteMonitorVersion|String|V1|The version of site monitoring. Valid values:

-   V1
-   V2 |
|Message|String|success|The returned message. |
|RequestId|String|26860260-76C6-404E-AB7A-EB98D36A6885|The ID of the request. |
|Success|String|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=DescribeSiteMonitorQuota
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeSiteMonitorQuotaResponse>
          <Message>success</Message>
          <RequestId>C1359088-B0D3-4344-BA51-FB920425D836</RequestId>
          <Data>
                <SiteMonitorVersion>V2</SiteMonitorVersion>
                <SiteMonitorQuotaTaskUsed>2</SiteMonitorQuotaTaskUsed>
                <SecondMonitor>false</SecondMonitor>
                <SiteMonitorOperatorQuotaQuota>0</SiteMonitorOperatorQuotaQuota>
                <SiteMonitorTaskQuota>100</SiteMonitorTaskQuota>
                <SiteMonitorIdcQuota>5</SiteMonitorIdcQuota>
          </Data>
          <Code>200</Code>
          <Success>true</Success>
</DescribeSiteMonitorQuotaResponse>
```

`JSON` format

```
{
    "Message":"success",
    "RequestId": "C1359088-B0D3-4344-BA51-FB920425D836",
    "Data": {
        "SiteMonitorVersion": "V2",
        "SiteMonitorQuotaTaskUsed": 2,
        "SecondMonitor": false,
        "SiteMonitorOperatorQuotaQuota": 0,
        "SiteMonitorTaskQuota": 100,
        "SiteMonitorIdcQuota": 5
    },
    "Code": "200",
    "Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

