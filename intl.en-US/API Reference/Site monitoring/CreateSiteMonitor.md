# CreateSiteMonitor

Creates a site monitoring task.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=CreateSiteMonitor&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|CreateSiteMonitor|The operation that you want to perform. Set the value to CreateSiteMonitor. |
|Address|String|Yes|https://www.aliyun.com|The URL or IP address monitored by the monitoring task. |
|TaskName|String|Yes|HanZhou\_ECS1|The name of the site monitoring task. The name must be 4 to 100 characters in length. It can contain letters, digits, and underscores \(\_\). |
|TaskType|String|Yes|HTTP|The protocol used by the site monitoring task. Valid values: HTTP, HTTPS, PING, TCP, UDP, DNS, SMTP, POP3, and FTP. |
|Interval|String|No|1|The interval at which detection requests are sent. Valid values: 1, 5, and 15. Unit: minutes. Default value: 1. |
|IspCities|String|No|\[\{"city":"546","isp":"465"\},\{"city":"572","isp":"465"\},\{"city":"738","isp":"465"\}\]|The information about detection points, which is specified in a JSON array. Example: `[{"city":"546","isp":"465"},{"city":"572","isp":"465"},{"city":"738","isp":"465"}]`. The three city codes represent Beijing, Hangzhou, and Qingdao.

 **Note:** You can call the DescribeSiteMonitorISPCityList API operation to query the detection points that can be used to create site monitoring tasks. For more information, see [DescribeSiteMonitorISPCityList](~~115045~~) . If this parameter is not specified, the system randomly selects three detection points for site monitoring. |
|OptionsJson|String|No|\{"time\_out":5000\}|The extended options of the protocol that is used by the site monitoring task. The options vary based on the protocol. |
|AlertIds|String|No|SystemDefault\_acs\_ecs\_dashboard\_InternetOutRate\_Percent|The ID of the alert rule. The ID of an existing alert rule to be associated with the site monitoring task. You can call the DescribeMetricRuleList API operation to query the IDs of existing alert rules. For more information, see [DescribeMetricRuleList](~~114941~~). |

The TaskType parameter specifies the following protocols that are used by a site monitoring task: HTTP, HTTPS, PING, TCP, UDP, DNS, SMTP. POP3, and FTP. The following tables describe the extended options of these protocols.

-   HTTP

|Parameter

|Type

|Description |
|-----------|------|-------------|
|http\_method

|String

|The request method. Valid values: GET, POST, and HEAD. Default value: GET. |
|header

|String

|The HTTP request header. The HTTP request header consists of key-value pairs. Separate the key-value pairs with line feeds \("\\n"\).

 Separate the key and value in each pair with a colon \(:\). |
|cookie

|String

|The HTTP cookie. Specify the HTTP cookie in compliance with the HTTP request standard. |
|request\_content

|String

|The content of the request. The content can be in JSON or form format. If this parameter is not specified, the request has no body. |
|response\_content

|String

|The expected or unexpected content of the response. The first 64 bytes of the content returned from the HTTP server will be checked during site monitoring. |
|match\_rule

|String

|The match rule. The value 0 indicates that the detection is successful if the response does not contain the unexpected content specified by the response\_content parameter.

 The value 1 indicates that the detection is successful if the response contains the expected content specified by the response\_content parameter. |
|username

|String

|The username used to authenticate the HTTP request. If this parameter is specified, the HTTP request contains the basic authentication header. |
|password

|String

|The password used to authenticate the HTTP request. |
|time\_out

|int

|The timeout period. Unit: milliseconds. Default value: 5. |
|max\_redirect

|int

|The maximum number of redirections. The default value is 5 for a detection point provided by Alibaba Cloud and 2 for a detection point provided by an Internet service provider \(ISP\).

 To disable redirections, set the value to 0.

 Valid values: 0 to 50. |

-   PING

|Parameter

|Type

|Description |
|-----------|------|-------------|
|failure\_rate

|int

|The failure rate threshold. If the failure rate exceeds this threshold, the detection fails and the status code 610 \(PingAllFail\) or 615 \(PingPartialFail\) is returned.

 Default value: 0.1. |
|ping\_num

|int

|The number of times that the monitored address is pinged. Default value: 20.

 Valid values: 1 to 100. |

-   DNS

|Parameter

|Type

|Description |
|-----------|------|-------------|
|dns\_server

|string

|The domain name or IP address of the Domain Name System \(DNS\) server. |
|dns\_type

|string

|The type of DNS records to query. Valid values: A, NS, CNAME, MX, TXT, and ANY. |
|expect\_value

|string

|The expected value list, which consists of the IP addresses to be obtained after DNS resolution. Separate the IP addresses with space characters. |
|match\_rule

|string

|The relationship between the expected value list and the returned value list after DNS resolution. If the two lists do not meet the specified relationship, the detection fails. Valid values:

 Empty string or IN\_DNS: The expected value list is a subset of the returned value list.

 DNS\_IN: The returned value list is a subset of the expected value list.

 EQUAL: The returned value list is the same as the expected value list.

 ANY: The returned value list intersects with the expected value list. |

-   FTP

|Parameter

|Type

|Description |
|-----------|------|-------------|
|port

|int

|The port number of the FTP server. If this parameter is not specified, the default port number is used. The default port number is 21 for FTP and 990 for FTPS. |
|username

|string

|The username used to log on to the FTP server. If this parameter is not specified, anonymous logon is used. |
|password

|string

|The password used to log on to the FTP server. |

-   POP3/SMTP

|Parameter

|Type

|Description |
|-----------|------|-------------|
|port

|int

|The port number of the POP3 server. The default port number is 110 for the POP3 protocol and 995 for the POP3S protocol. |
|username

|string

|The username used to log on to the POP3 or SMTP server. |
|password

|string

|The password used to log on to the POP3 or SMTP server. |

-   TCP/UDP

|Parameter

|Type

|Description |
|-----------|------|-------------|
|port

|int

|The TCP or UDP port to monitor. |
|request\_content

|string

|The content of the request. If the request\_format parameter is set to hex, the value of the request\_content parameter must be in the hexadecimal format. |
|request\_format

|string

|The format of the request content. If the request\_format parameter is not set to hex, the value of the request\_content parameter is be sent to the POP3 or SMTP server as common text. |
|response\_content

|string

|The expected or unexpected content of the response. If the response from the POP3 or SMTP server does not contain the expected content specified by the response\_content parameter, the detection fails.

 If the response\_format parameter is set to hex, the value of the response\_content parameter must be in the hexadecimal format.

 If the response\_format parameter is not set to hex, the server considers the value of the response\_content parameter as common text. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|AlertRule|String|\[\{"alarmActions":\["Default alert group"\],"metricName":"Availability","expression":"$Availability<96"\}\]|The alert rule configured for the site monitoring task. The value is a JSON array in the following format:

 `[{"alarmActions":["xxx"],"metricName":"Availability","expression":"$Availability<96"}]`.

 -   alarmActions: the alert group to which alert notifications are sent.
-   metricName: the name of the metric that triggers alerts. Valid values:
    -   Availability: the percentage of available detection points.
    -   AvailableNumber: the number of available detection points. |
|Code|String|200|The HTTP status code.

 **Note:** The status code 200 indicates that the call was successful. |
|CreateResultList|Array of CreateResultList| |The results of creating site monitoring tasks. After a task is created, the corresponding result is returned. |
|CreateResultList| | | |
|TaskId|String|df1f48e3-f814-491a-ad5f-\*\*\*\*|The ID of the site monitoring task. |
|TaskName|String|HanZhou\_ECS1|The name of the site monitoring task. |
|Data|Struct| |The result of creating the site monitoring task. |
|AttachAlertResult|Array of Contact| |The result of associating the existing alert rule with the site monitoring task. |
|Contact| | | |
|Code|String|200|The HTTP status code returned after a request was sent to associate the existing alert rule with the site monitoring task.

 **Note:** The status code 200 indicates that the call was successful. |
|Message|String|successful|The message returned after a request was sent to associate the existing alert rule with the site monitoring task. |
|RequestId|String|32565d-233-1b98-2231-892813f86c71|The ID of the request that was sent to associate the existing alert rule with the site monitoring task. |
|RuleId|String|SystemDefault\_acs\_ecs\_dashboard\_InternetOutRate\_Percent|The ID of the existing alert rule that was associated with the site monitoring task. |
|Success|String|true|Indicates whether the existing alert rule was associated with the site monitoring task. Valid values:

 -   true: The association was successful.
-   false: The association failed. |
|Message|String|Successful|The returned message. |
|RequestId|String|68192f5d-0d45-4b98-9724-892813f86c71|The ID of the request. |
|Success|String|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=CreateSiteMonitor
&Address=https://www.aliyun.com
&TaskName=HanZhou_ECS1
&TaskType=HTTP
&<Common request parameters>
```

Sample success responses

`XML` format

```
<CreateSiteMonitorResponse>
	  <Message>successful</Message>
	  <RequestId>AB22040B-D13E-4693-9FE8-741615F5CBFC</RequestId>
	  <Data>
		    <AttachAlertResult>
			      <Contact>
				        <Message>successful</Message>
				        <RequestId>5dd33455-4f65-4b0c-9200-33d66f3f340b</RequestId>
				        <RuleId>SystemDefault_acs_ecs_dashboard_InternetOutRate_Percent</RuleId>
				        <Code>200</Code>
				        <Success>true</Success>
			      </Contact>
		    </AttachAlertResult>
	  </Data>
	  <Code>200</Code>
	  <CreateResultList>
		    <CreateResultList>
			      <TaskId>2c8dbdf9-a3ab-46a1-85a4-f094965ebef9</TaskId>
			      <TaskName>HanZhou_ECS1</TaskName>
		    </CreateResultList>
	  </CreateResultList>
	  <Success>true</Success>
</CreateSiteMonitorResponse>
```

`JSON` format

```
{
	"Message": "successful",
	"RequestId": "AB22040B-D13E-4693-9FE8-741615F5CBFC",
	"Data": {
		"AttachAlertResult": {
			"Contact": [
				{
					"Message": "successful",
					"RequestId": "5dd33455-4f65-4b0c-9200-33d66f3f340b",
					"RuleId": "SystemDefault_acs_ecs_dashboard_InternetOutRate_Percent",
					"Code": "200",
					"Success": true
				}
			]
		}
	},
	"Code": "200",
	"CreateResultList": {
		"CreateResultList": [
			{
				"TaskId": "2c8dbdf9-a3ab-46a1-85a4-f094965ebef9",
				"TaskName": "HanZhou_ECS1"
			}
		]
	},
	"Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

