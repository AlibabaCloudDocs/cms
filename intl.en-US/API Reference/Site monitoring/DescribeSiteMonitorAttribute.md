# DescribeSiteMonitorAttribute

Queries the details about a site monitoring task.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeSiteMonitorAttribute&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeSiteMonitorAttribute|The operation that you want to perform. Set the value to DescribeSiteMonitorAttribute. |
|TaskId|String|Yes|a1ecd34a-8157-44d9-b065-14950837\*\*\*\*|The ID of the site monitoring task whose details are to be queried. |
|IncludeAlert|Boolean|No|false|Specifies whether to return the information about the alert rules configured for the site monitoring task.

-   The value `true` indicates that alert rule information will be returned.
-   The value `false` indicates that alert rule information will not be returned. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|9ed350c5-d579-4ba1-9c5d-dda70cd8422c|The ID of the request. |
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Success|Boolean|true|Indicates whether the call was successful. |
|SiteMonitors|N/A|N/A|The details about the site monitoring task. |
|Address|String|http://www.aliyun.com|The address monitored by the site monitoring task. |
|Interval|String|1|The interval at which detection requests are sent to the monitored address. Unit: minutes. Valid values: 1, 5, and 15. |
|IspCities|Array|N/A|The detection point information, including the carriers that provide the detection points and cities where the detection points reside. |
|IspCity|N/A|N/A|The carrier and city of a detection point. |
|City|String|546|The ID of the city. |
|CityName|String|Hangzhou|The name of the city. |
|Isp|String|465|The ID of the carrier. |
|IspName|String|Alibaba Cloud|The name of the carrier. |
|OptionJson|Json|\{ "http\_method": "get", "response\_content": "xxxx", "time\_out": 30000\}|The extended options of the protocol used by the site monitoring task. The options vary based on the protocol. For more information, see the description of extended options in [CreateSiteMonitor](~~115048~~). |
|TaskId|String|a1ecd34a-8157-44d9-b060-14950837\*\*\*\*|The ID of the site monitoring task. |
|TaskName|String|Task name|The name of the site monitoring task. |
|TaskState|String|OK|The status of the site monitoring task. |
|TaskType|String|HTTP|The protocol used by the site monitoring task. Valid values: HTTP, PING, TCP, UDP, SMTP, POP3, DNS, and FTP. |
|MetricRules|Array|N/A|The alert rules configured for the site monitoring task. |
|MetricRule|N/A|N/A|The information about an alert rule configured for the site monitoring task. |
|ActionEnable|String|true|Indicates whether the alert rule was enabled. |
|AlarmActions|String|\["Alert group"\]|The alert group to which alert notifications are sent when the alert rule is in the ALARM state. |
|ComparisonOperator|String|\>|The comparison operator. |
|Dimensions|String|\[ \{ "taskId": "49f7b317-7645-4cc9-94fd-ea42e522\*\*\*\*" \} \]|The dimension of the alert rule. |
|EvaluationCount|String|3|The consecutive number of times for which the metric value is measured before an alert is triggered. |
|Expression|String|$Availability\>90|The expression of the alert rule. |
|Level|String|3|The level of the alert. |
|MetricName|String|Availability|The name of the metric. |
|Namespace|String|acs\_networkmonitor|The namespace of the service.

Specify the value in the format of acs\_Service name. |
|OkActions|String|\["Alert group"\]|The alert group to which alert notifications are sent when the alert rule is in the OK state. |
|Period|String|60|The time interval at which monitoring data is queried. Generally, the time interval equals the frequency for reporting metric data. Unit: seconds.

**Note:** If a statistical period was specified for the alert rule, raw data will be queried based on the statistical period. |
|RuleId|String|49f7b317-7645-4cc1-94fd-ea42e5220932\_Availability|The ID of the alert rule. |
|RuleName|String|Availability|The name of the alert rule. |
|StateValue|String|OK|The status of the alert rule. Valid values:

-   `OK`: No alert was triggered based on the alert rule.
-   `ALARM`: An alert was triggered based on the alert rule. |
|Statistics|String|Availability|The statistical method of the alert rule. |
|Threshold|String|90|The threshold for triggering alerts. |
|Message|String|Successful|The returned message. |

## Examples

Sample requests

```

http(s)://[Endpoint]/? Action=DescribeSiteMonitorAttribute
&TaskId=a1ecd34a-8157-44d9-b065-14950837****
&<Common request parameters>

```

Sample success responses

`XML` format

```
<Message>Successful</Message>
<RequestId>baac6ca7-8152-4156-987a-653a1533f0e5</RequestId>
<SiteMonitors>
    <OptionJson>
        <http_method>get</http_method>
        <response_content>xxxx</response_content>
        <time_out>30000</time_out>
    </OptionJson>
    <Interval>1</Interval>
    <Address>http://www.aliyun.com</Address>
    <TaskId>a1ecd34a-8157-44d9-b060-1****</TaskId>
    <TaskName>Task name</TaskName>
    <TaskState>1</TaskState>
    <TaskType>HTTP</TaskType>
    <IspCities>
        <IspCity>
            <Isp>465</Isp>
            <IspName>Alibaba Cloud</IspName>
            <CityName>Hangzhou</CityName>
            <City>546</City>
        </IspCity>
        <IspCity>
            <Isp>465</Isp>
            <IspName>Alibaba Cloud</IspName>
            <CityName>Qingdao</CityName>
            <City>572</City>
        </IspCity>
        <IspCity>
            <Isp>465</Isp>
            <IspName>Alibaba Cloud</IspName>
            <CityName>Beijing</CityName>
            <City>738</City>
        </IspCity>
    </IspCities>
</SiteMonitors>
<Success>true</Success>
<Code>200</Code>
```

`JSON` format

```
{
	"Message":"Successful",
	"RequestId":"baac6ca7-8152-4156-987a-653a1533f0e5",
	"Success":true,
	"SiteMonitors":{
		"OptionJson":{
			"http_method":"get",
			"response_content":"xxxx",
			"time_out":30000
		},
		"Interval":1,
		"Address":"http://www.aliyun.com",
		"TaskId":"a1ecd34a-8157-44d9-b060-1****",
		"TaskType":"HTTP",
		"TaskState":1,
		"TaskName":"Task name",
		"IspCities":{
			"IspCity":[
				{
					"Isp":"465",
					"IspName":"Alibaba Cloud",
					"CityName":"Hangzhou",
					"City":"546"
				},
				{
					"Isp":"465",
					"IspName":"Alibaba Cloud",
					"CityName":"Qingdao",
					"City":"572"
				},
				{
					"Isp":"465",
					"IspName":"Alibaba Cloud",
					"CityName":"Beijing",
					"City":"738"
				}
			]
		}
	},
	"Code":"200"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

