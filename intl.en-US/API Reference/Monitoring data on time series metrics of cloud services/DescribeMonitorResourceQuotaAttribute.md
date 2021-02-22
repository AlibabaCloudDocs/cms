# DescribeMonitorResourceQuotaAttribute

Queries the resource quotas of Cloud Monitor.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeMonitorResourceQuotaAttribute&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeMonitorResourceQuotaAttribute|The operation that you want to perform. Set the value to DescribeMonitorResourceQuotaAttribute. |
|ShowUsed|Boolean|No|true|Specifies whether to return the information about used quotas. Valid values:

-   true: This is the default value.
-   false |

For more information about common request parameters, see [Common parameters](~~199331~~).

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

**Note:** The HTTP status code 200 indicates a success. |
|Message|String|The specified resource is not found.|The error message. |
|RequestId|String|31BC7201-00F2-47B2-B7B9-6A173076ACE|The ID of the request. |
|ResourceQuota|Struct| |The details about the resource quotas of Cloud Monitor. |
|Api|Struct| |The details about the quota of API operation calls. |
|QuotaLimit|Integer|500|The total quota of API operation calls. The product of multiplying the value and 10,000 indicates the total quota. |
|QuotaPackage|Integer|500|The quota of API operation calls in your purchased plan. The product of multiplying the value and 10,000 indicates the quota. |
|QuotaUsed|Integer|9987|The used quota of API operation calls in your purchased plan. Unit: API operation call. |
|CustomMonitor|Struct| |The details about the quota of custom monitoring. |
|QuotaLimit|Integer|1200|The total quota of the time series in custom monitoring. Unit: time series. |
|QuotaPackage|Integer|1000|The quota of the time series in custom monitoring in your purchased plan. Unit: time series. |
|QuotaUsed|Integer|8|The used quota of the time series in custom monitoring in your purchased plan. Unit: time series. |
|EventMonitor|Struct| |The details about the quota of event monitoring. |
|QuotaLimit|Integer|55|The total quota of events that can be reported in event monitoring. The product of multiplying the value and 10,000 indicates the total quota. |
|QuotaPackage|Integer|50|The quota of events that can be reported in event monitoring in your purchased plan. The product of multiplying the value and 10,000 indicates the quota. |
|QuotaUsed|Integer|2|The used quota of events that can be reported in event monitoring in your purchased plan. The product of multiplying the value and 10,000 indicates the used quota. |
|ExpireTime|String|2021-02-28|The time when the plan expires. |
|InstanceId|String|cms\_edition-cn-n6w20rn\*\*\*\*|The ID of the purchased subscription plan. |
|LogMonitor|Struct| |The details about the quota of log monitoring. |
|QuotaLimit|Integer|150|The total quota of processed log data in log monitoring. Unit: MB/min. |
|QuotaPackage|Integer|150|The quota of processed log data in log monitoring in your purchased plan. Unit: MB/min. |
|QuotaUsed|Integer|80|The used quota of processed log data in log monitoring in your purchased plan. Unit: MB/min. |
|Phone|Struct| |The details about the quota of alert phone calls. |
|QuotaLimit|Integer|550|The total quota of alert phone calls. Unit: phone call. |
|QuotaPackage|Integer|500|The quota of alert phone calls in your purchased resource plan. Unit: phone call. |
|QuotaUsed|Integer|100|The used quota of alert phone calls in your purchased resource plan. Unit: phone call. |
|SMS|Struct| |The details about the quota of alert text messages. |
|QuotaLimit|Integer|550|The total quota of alert text messages. Unit: text message. |
|QuotaPackage|Integer|500|The quota of alert text messages in your purchased resource plan. Unit: text message. |
|QuotaUsed|Integer|38|The used quota of alert text messages in your purchased resource plan. Unit: text message. |
|SiteMonitorEcsProbe|Struct| |The details about the quota of detection points that are provided by Alibaba Cloud in site monitoring. |
|QuotaLimit|Integer|5|The total quota of detection points that are provided by Alibaba Cloud in site monitoring.

**Note:** The value indicates the maximum number of detection points provided by Alibaba Cloud that can be selected for a site monitoring task. |
|QuotaPackage|Integer|5|The quota of detection points that are provided by Alibaba Cloud in site monitoring in your purchased plan. |
|QuotaUsed|Integer|20|The used quota of detection points that are provided by Alibaba Cloud in site monitoring in your purchased plan.

**Note:** The value indicates the total number of detection points provided by Alibaba Cloud that are selected by existing site monitoring tasks. |
|SiteMonitorOperatorProbe|Struct| |The details about the quota of detection points that are provided by other carriers in site monitoring. |
|QuotaLimit|Integer|5|The total quota of detection points that are provided by other carriers in site monitoring. |
|QuotaPackage|Integer|5|The quota of detection points that are provided by other carriers in site monitoring in your purchased plan. |
|QuotaUsed|Integer|0|The used quota of detection points that are provided by other carriers in site monitoring in your purchased plan. |
|SiteMonitorTask|Struct| |The quota of site monitoring tasks. |
|QuotaLimit|Integer|25|The total quota of site monitoring tasks. Unit: site monitoring task. |
|QuotaPackage|Integer|20|The quota of site monitoring tasks in your purchased plan. Unit: site monitoring task. |
|QuotaUsed|Integer|15|The used quota of site monitoring tasks in your purchased plan. Unit: site monitoring task. |
|SuitInfo|String|pro|The current edition of Cloud Monitor. Valid values:

-   free: the free edition.
-   pro: Professional Edition.
-   cms\_post: pay-as-you-go. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DescribeMonitorResourceQuotaAttribute
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeMonitorResourceQuotaAttributeResponse>
      <RequestId>1E1961C4-B340-45D7-8CC3-F7D0BF19F2E0</RequestId>
      <ResourceQuota>
            <SiteMonitorOperatorProbe>
                  <QuotaUsed>0</QuotaUsed>
                  <QuotaPackage>5</QuotaPackage>
                  <QuotaLimit>5</QuotaLimit>
            </SiteMonitorOperatorProbe>
            <InstanceId>cms_edition-cn-n6w20rn****</InstanceId>
            <Phone>
                  <QuotaUsed>100</QuotaUsed>
                  <QuotaPackage>500</QuotaPackage>
                  <QuotaLimit>550</QuotaLimit>
            </Phone>
            <SuitInfo>pro</SuitInfo>
            <SiteMonitorTask>
                  <QuotaUsed>7</QuotaUsed>
                  <QuotaPackage>20</QuotaPackage>
                  <QuotaLimit>20</QuotaLimit>
            </SiteMonitorTask>
            <SMS>
                  <QuotaUsed>38</QuotaUsed>
                  <QuotaPackage>500</QuotaPackage>
                  <QuotaLimit>550</QuotaLimit>
            </SMS>
            <LogMonitor>
                  <QuotaUsed>0</QuotaUsed>
                  <QuotaPackage>50</QuotaPackage>
                  <QuotaLimit>50</QuotaLimit>
            </LogMonitor>
            <Api>
                  <QuotaUsed>9987</QuotaUsed>
                  <QuotaPackage>500</QuotaPackage>
                  <QuotaLimit>500</QuotaLimit>
            </Api>
            <ExpireTime>2021-02-28</ExpireTime>
            <SiteMonitorEcsProbe>
                  <QuotaUsed>20</QuotaUsed>
                  <QuotaPackage>5</QuotaPackage>
                  <QuotaLimit>5</QuotaLimit>
            </SiteMonitorEcsProbe>
            <CustomMonitor>
                  <QuotaUsed>8</QuotaUsed>
                  <QuotaPackage>1000</QuotaPackage>
                  <QuotaLimit>1200</QuotaLimit>
            </CustomMonitor>
            <EventMonitor>
                  <QuotaUsed>2</QuotaUsed>
                  <QuotaPackage>50</QuotaPackage>
                  <QuotaLimit>55</QuotaLimit>
            </EventMonitor>
      </ResourceQuota>
      <Code>200</Code>
</DescribeMonitorResourceQuotaAttributeResponse>
```

`JSON` format

```
{
    "RequestId": "1E1961C4-B340-45D7-8CC3-F7D0BF19F2E0",
    "ResourceQuota": {
        "SiteMonitorOperatorProbe": {
            "QuotaUsed": 0,
            "QuotaPackage": 5,
            "QuotaLimit": 5
        },
        "InstanceId": "cms_edition-cn-n6w20rn****",
        "Phone": {
            "QuotaUsed": 100,
            "QuotaPackage": 500,
            "QuotaLimit": 550
        },
        "SuitInfo": "pro",
        "SiteMonitorTask": {
            "QuotaUsed": 7,
            "QuotaPackage": 20,
            "QuotaLimit": 20
        },
        "SMS": {
            "QuotaUsed": 38,
            "QuotaPackage": 500,
            "QuotaLimit": 550
        },
        "LogMonitor": {
            "QuotaUsed": 0,
            "QuotaPackage": 50,
            "QuotaLimit": 50
        },
        "Api": {
            "QuotaUsed": 9987,
            "QuotaPackage": 500,
            "QuotaLimit": 500
        },
        "ExpireTime": "2021-02-28",
        "SiteMonitorEcsProbe": {
            "QuotaUsed": 20,
            "QuotaPackage": 5,
            "QuotaLimit": 5
        },
        "CustomMonitor": {
            "QuotaUsed": 8,
            "QuotaPackage": 1000,
            "QuotaLimit": 1200
        },
        "EventMonitor": {
            "QuotaUsed": 2,
            "QuotaPackage": 50,
            "QuotaLimit": 55
        }
    },
    "Code": 200
}
```

## Error codes

|HTTP status code|Error code|Error message|Description|
|----------------|----------|-------------|-----------|
|404|ResourceNotFound|The specified resource is not found.|The error message returned because the specified resource is not found.|

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

