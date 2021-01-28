# CreateSiteMonitor

Creates a site monitoring task.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=CreateSiteMonitor&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|CreateSiteMonitor|The operation that you want to perform. Set the value to CreateSiteMonitor. |
|Address|String|Yes|https://www.aliyun.com|The URL or IP address monitored by the monitoring task. |
|TaskName|String|Yes|HanZhou\_ECS1|The name of the monitoring task. The name must be 4 to 100 characters in length. It can contain letters, digits, and underscores \(\_\). |
|TaskType|String|Yes|HTTP|The type of the monitoring task. Valid values: HTTP, HTTPS, PING, TCP, UDP, DNS, SMTP, POP3, and FTP. |
|Interval|String|No|1|The interval at which detection requests are sent. Valid values: 1, 5, and 15. Unit: minutes. Default value: 1. |
|IspCities|String|No|\[\{"city":"546","isp":"465"\},\{"city":"572","isp":"465"\},\{"city":"738","isp":"465"\}\]|The information about the detection points, in the format of a JSON array. Example: `[{"city":"546","isp":"465"},{"city":"572","isp":"465"},{"city":"738","isp":"465"}]`. The values of the city field indicate Beijing, Hangzhou, and Qingdao.

**Note:** You can call the DescribeSiteMonitorISPCityList operation to query the detection points. For more information, see [DescribeSiteMonitorISPCityList](~~115045~~). If this parameter is not specified, the system randomly selects three detection points. |
|OptionsJson|String|No|\{"time\_out":5000\}|The extended options of the protocol that is used by the monitoring task. The options vary based on the protocol. |
|AlertIds|String|No|SystemDefault\_acs\_ecs\_dashboard\_InternetOutRate\_Percent|The ID of the alert rule. You can call the DescribeMetricRuleList operation to query the IDs of existing alert rules in Cloud Monitor. For more information, see [DescribeMetricRuleList](~~114941~~). |

The following tables describe the extended options of the HTTP, HTTPS, PING, TCP, UDP, DNS, SMTP. POP3, and FTP protocols specified by the TaskType parameter.

-   HTTP

|Parameter

|Type

|Description |
|-----------|------|-------------|
|http\_method

|String

|The HTTP request method. Valid values: GET, POST, and HEAD. Default value: GET. |
|header

|String

|The custom HTTP headers that are separated with newline characters \(\\n\).

Each header must comply with the HTTP protocol. Each header must be a key-value pair in which the key and value are separated with a colon \(:\). |
|cookie

|String

|The HTTP cookie that is specified in compliance with the HTTP request standard. |
|request\_content

|String

|The content of the request. The content can be in the JSON or form format. If this parameter is not specified, the request has no body. |
|response\_content

|String

|The expected content of the response. The first 64 bytes of the content returned by the HTTP server are checked during site monitoring. |
|match\_rule

|String

|The value 0 indicates that the detection is successful if the response does not contain the content specified by the response\_content parameter.

The value 1 indicates that the detection is successful if the response contains the content specified by the response\_content parameter. |
|username

|String

|If the username parameter is specified, the HTTP request contains the basic authentication header. |
|password

|String

|The password used to authenticate the HTTP request. |
|time\_out

|Integer

|The timeout period. Unit: milliseconds. Default value: 5. |
|max\_redirect

|Integer

|The maximum number of redirections. The default value is 5 for a detection point that is running on an Elastic Compute Service \(ECS\) instance and 2 for a detection point that is provided by a carrier.

To disable redirections, set the value to 0.

Valid values: 0 to 50. |

-   PING

|Parameter

|Type

|Description |
|-----------|------|-------------|
|failure\_rate

|Integer

|If the failure rate of the ping operation exceeds the value of this parameter, the detection fails and the status code 610 or 615 is returned. The error message of the status code 610 is PingAllFail, whereas the error message of the status code 615 is PingPartialFail.

Default value: 0.1. |
|ping\_num

|Integer

|The number of times that the monitored address is pinged. Default value: 20.

Valid values: 1 to 100. |

-   DNS

|Parameter

|Type

|Description |
|-----------|------|-------------|
|dns\_server

|String

|The domain name or IP address of the Domain Name System \(DNS\) server. |
|dns\_type

|String

|The type of the DNS records to query. Valid values: A, NS, CNAME, MX, TXT, and ANY. |
|expect\_value

|String

|The list of expected values. Separate the expected values with space characters. |
|match\_rule

|String

|The relationship between the list of expected values and the list of DNS results. If the two lists do not meet the specified relationship, the detection fails. Valid values:

Empty string or IN\_DNS: The list of expected values is a subset of the list of DNS results.

DNS\_IN: The list of DNS results is a subset of the list of expected values.

EQUAL: The list of DNS results is the same as the list of expected values.

ANY: The list of DNS results intersects with the list of expected values. |

-   FTP

|Parameter

|Type

|Description |
|-----------|------|-------------|
|port

|Integer

|The port number of the FTP server. If this parameter is not specified, the default value is used. The default port number is 21 for FTP and 990 for FTPS. |
|username

|String

|The username used to log on to the FTP server. If this parameter is not specified, anonymous logon is used. |
|password

|String

|The password used to log on to the FTP server. |

-   POP3/SMTP

|Parameter

|Type

|Description |
|-----------|------|-------------|
|port

|Integer

|The port number of the POP3 server. The default port number is 110 for POP3 and 995 for POP3S. |
|username

|String

|The username used to log on to the POP3 or SMTP server. |
|password

|String

|The password used to log on to the POP3 or SMTP server. |

-   TCP/UDP

|Parameter

|Type

|Description |
|-----------|------|-------------|
|port

|Integer

|The port number of the TCP or UDP server. |
|request\_content

|String

|The content of the request. If the request\_format parameter is set to hex, the value of the request\_content parameter is parsed in the hexadecimal format. |
|request\_format

|String

|If the request\_format parameter is set to another value, the value of the request\_content parameter is sent to the TCP or UDP server as a regular string. |
|response\_content

|String

|The content of the response. If the response from the TCP or UDP server does not contain the content specified by the response\_content parameter, the detection fails.

If the response\_format parameter is set to hex, the value of the response\_content parameter is parsed in the hexadecimal format.

If the response\_format parameter is set to another value, the value of the response\_content parameter is parsed as a regular string. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|CreateResultList|Array of CreateResultList| |The results of creating tasks. If a task is created, the result is returned. If a task fails to be created, no result is returned. |
|CreateResultList| | | |
|TaskId|String|2c8dbdf9-a3ab-46a1-85a4-f094965e\*\*\*\*|The ID of the monitoring task. |
|TaskName|String|HanZhou\_ECS1|The name of the monitoring task. |
|Data|Struct| |The result of creating the monitoring task. |
|AttachAlertResult|Array of Contact| |The result of associating the existing alert rule with the site monitoring task. |
|Contact| | | |
|Code|String|200|The status code returned after you associate the existing alert rule with the site monitoring task.

**Note:** The status code 200 indicates that the association was successful. |
|Message|String|successful|The message returned after you associate the existing alert rule with the site monitoring task. |
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
                  <TaskId>2c8dbdf9-a3ab-46a1-85a4-f094965e****</TaskId>
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
                "TaskId": "2c8dbdf9-a3ab-46a1-85a4-f094965e****",
                "TaskName": "HanZhou_ECS1"
            }
        ]
    },
    "Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

