# DescribeAlertLogList

Queries alert logs.

This topic provides an example on how to query the alert logs of Elastic Compute Service \(ECS\) from the cloud service dimension.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeAlertLogList&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeAlertLogList|The operation that you want to perform. Set the value to DescribeAlertLogList. |
|StartTime|Long|No|1609988009694|The start timestamp of the alert logs to be queried. Unit: milliseconds. |
|EndTime|Long|No|1610074409694|The end timestamp of the alert logs to be queried. Unit: milliseconds. |
|PageNumber|Integer|No|1|The number of the page to return. Default value: 1 |
|PageSize|Integer|No|10|The number of entries to return on each page. Default value: 10. |
|SearchKey|String|No|alert|The keyword based on which the alert logs to be queried are searched. |
|GroupId|String|No|7301\*\*\*\*|The ID of the application group. |
|Namespace|String|No|acs\_ecs\_dashboard|The namespace of the cloud service.

**Note:** For more information about the namespaces of cloud services, see [Appendix 1: Metrics](~~163515~~). |
|Product|String|No|ECS|The abbreviation of the service name. |
|Level|String|No|P4|The level and notification method of the alert. Valid values:

-   P4: Alert notifications are sent by using emails and DingTalk chatbots.
-   OK: No alert is generated. |
|SendStatus|String|No|0|The status of the alert. Valid values:

-   0: The alert is triggered or cleared.
-   1: The alert is generated not during the effective period.
-   2: The alert is muted and not triggered in a specified period.
-   3: The host is restarting.
-   4: Notifications are not sent for the alert.

When the value of the SendStatus parameter is 0, the value P4 of the Level parameter indicates a triggered alert and the value OK indicates a cleared alert. |
|ContactGroup|String|No|ECS\_Group|The alert group. |
|RuleName|String|No|test123|The name of the alert rule. |
|MetricName|String|No|IntranetInRate|The name of the metric.

**Note:** For more information about the metrics of different cloud services, see [Appendix 1: Metrics](~~163515~~). |
|LastMin|String|No|360|The statistical period of alert logs. Unit: minutes. |
|GroupBy|String|No|product|The dimension based on which data is aggregated. This parameter is similar to the Group By clause of SQL statements. Valid values:

-   `product`: aggregates data by cloud service.
-   `level`: aggregates data by alert level.
-   `groupId`: aggregates data by application group.
-   `contactGroup`: aggregates data by alert group.
-   `product,metricName`: aggregates data both by cloud service and by metric. |

For more information about common request parameters, see [Common parameters](~~199331~~).

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|AlertLogList|Array of Alarm|N/A|The details about alert logs. |
|AlertTime|String|1610043776621|The timestamp when the alert was triggered. Unit: milliseconds. |
|ContactALIIWWList|List|Alice|The TradeManager IDs of alert contacts.

**Note:** This parameter can be returned only on the China site \(aliyun.com\). |
|ContactDingList|List|CloudMonitor|The DingTalk chatbots of alert contacts. |
|ContactGroups|List|ECS\_Group|The alert group. |
|ContactMailList|List|alice@example.com|The email addresses of alert contacts. |
|ContactOnCallList|List|1368888\*\*\*\*|The phone numbers of alert contacts that can receive alert phone calls.

**Note:** This parameter can be returned only on the China site \(aliyun.com\). |
|ContactSMSList|List|1368888\*\*\*\*|The phone numbers of alert contacts that can receive alert text messages.

**Note:** This parameter can be returned only on the China site \(aliyun.com\). |
|Dimensions|Array of Dimensions|N/A|The dimensions of the resource that trigger alerts. |
|Key|String|instanceId|The key of the dimension of the resource that triggered alerts. |
|Value|String|i-m5e1qg6uo38rztr4\*\*\*\*|The value of the dimension of the resource that triggered alerts. |
|DingdingWebhookList|List|https://oapi.dingtalk.com/robot/send?access\_token=b7ff24032da1a5f86659ecda46797e13cc1d4e4da6903d7b014ea1d1488b\*\*\*\*|The webhook URLs of alert contacts. |
|Escalation|Struct|N/A|The alert rule based on which the alert is triggered. |
|Expression|String|$Average<90|The description of the alert rule.

**Note:** The content of the alert rule. This value indicates the conditions that trigger an alert. |
|Level|String|P4|The level and notification method of the alert. Valid values:

-   P4: Alert notifications are sent by using emails and DingTalk chatbots.
-   OK: No alert is generated. |
|Times|Integer|1|The consecutive number of times for which the metric value was measured before the alert was triggered. |
|EventName|String|IOHang|The name of the custom event. |
|ExtendedInfo|Array of ExtInfo|N/A|The extended information about the alert. |
|Name|String|userId|The name of the extended field. |
|Value|String|12706\*\*\*\*|The value of the extended field. |
|GroupId|String|7301\*\*\*\*|The ID of the application group. |
|GroupName|String|ECS\_Instances|The name of the application group. |
|InstanceId|String|i-m5e1qg6uo38rztr4\*\*\*\*|The ID of the resource. |
|InstanceName|String|portalHost|The name of the resource. |
|Level|String|P4|The level and notification method of the alert. Valid values:

-   P4: Alert notifications are sent by using emails and DingTalk chatbots.
-   OK: No alert is generated. |
|LevelChange|String|P4-\>OK|The change of the alert level. Valid values:

-   `P4->OK`: The alert level was changed from P4 to OK.
-   `P4->P4`:The alert level was still P4. |
|Message|String|\{"alertName":"e47aa0ac-4076-44db-a47d-d1083968\*\*\*\*\_Availability"\}|The alert information in a JSON string. |
|MetricName|String|cpu\_total|The name of the metric. |
|Namespace|String|acs\_ecs\_dashboard|The namespace of the cloud service. |
|Product|String|ECS|The identifier of the cloud service. Valid values:

-   If the cloud service is provided by Alibaba Cloud, the abbreviation of the service name is returned. Example: ECS.
-   If the cloud service is not provided by Alibaba Cloud, a value in the `acs_Service keyword` format is returned. Example: acs\_networkmonitor. |
|RuleId|String|d582b9e9-b1c1-4f17-9279-0fe7333a\*\*\*\*\_ResponseTime|The ID of the alert rule. |
|RuleName|String|CPU utilization|The name of the alert rule. |
|SendStatus|String|0|The status of the alert. Valid values:

-   0: The alert is triggered or cleared.
-   1: The alert is generated not during the effective period.
-   2: The alert is muted and not triggered in a specified period.
-   3: The host is restarting.
-   4: Notifications are not sent for the alert.

When the value of the SendStatus parameter is 0, the value P4 of the Level parameter indicates a triggered alert and the value OK indicates a cleared alert. |
|WebhookList|List|https://www.aliyun.com|The callback URLs to which alert notifications are sent. |
|Code|String|200|The HTTP status code.

**Note:** The HTTP status code 200 indicates a success. |
|Message|String|The specified resource is not found.|The error message. |
|PageNumber|Integer|1|The number of the returned page. |
|PageSize|Integer|10|The number of entries returned on each page. |
|RequestId|String|1C4A3709-BF52-42EE-87B5-7435F0929585|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |
|Total|Integer|88|The total number of returned entries. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DescribeAlertLogList
&Product=ECS
&GroupBy=product
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeAlertLogListResponse>
      <AlertLogList>
            <GroupName></GroupName>
            <Message>{\"alertName\":\"d582b9e9-b1c1-4f17-9279-0fe7333a****_ResponseTime\",\"curLevel\":\"OK\",\"dimensions\":{\"taskId\":\"d582b9e9-b1c1-4f17-9279-0fe7333a****\",\"userId\":\"127067667954****\"},\"escalation\":{\"expression\":\"$Average&gt;=800\",\"level\":P4,\"tag\":\"P4\",\"times\":1}</Message>
            <RuleId>d582b9e9-b1c1-4f17-9279-0fe7****_ResponseTime</RuleId>
            <Escalation>
                  <Expression>$Average&gt;=800</Expression>
                  <Times>1</Times>
                  <Level>P4</Level>
            </Escalation>
            <SendStatus>0</SendStatus>
            <Product>acs_ecs_dashboard</Product>
            <MetricName>cpu_total</MetricName>
            <RuleName>CPU utilization</RuleName>
            <ContactGroups>ECS_Group</ContactGroups>
            <InstanceId></InstanceId>
            <LevelChange>P4-&gt;OK</LevelChange>
            <Dimensions>
                  <Value>127067667954****</Value>
                  <Key>userId</Key>
            </Dimensions>
            <Dimensions>
                  <Value>i-abcdefgh12****</Value>
                  <Key>instanceId</Key>
            </Dimensions>
            <EventName>AlertOk</EventName>
            <ExtendedInfo>
                  <Value>i-hp34y1eiszazu49y****</Value>
                  <Name>instanceId</Name>
            </ExtendedInfo>
            <ExtendedInfo>
                  <Value>12706****</Value>
                  <Name>userId</Name>
            </ExtendedInfo>
            <Namespace>acs_ecs_dashboard</Namespace>
            <AlertTime>1610085521564</AlertTime>
            <GroupId>7301****</GroupId>
            <InstanceName>portalHost</InstanceName>
            <Level>OK</Level>
      </AlertLogList>
      <RequestId>6FCB1AB7-57F7-4DDA-B14E-6468FAFE79D9</RequestId>
      <PageSize>10</PageSize>
      <PageNumber>1</PageNumber>
      <Code>200</Code>
      <Success>true</Success>
</DescribeAlertLogListResponse>
```

`JSON` format

```
{
    "AlertLogList": [
        {
            "GroupName": "",
            "ContactALIIWWList": [],
            "Message": "{\"alertName\":\"d582b9e9-b1c1-4f17-9279-0fe7333a****_ResponseTime\",\"curLevel\":\"OK\",\"dimensions\":{\"taskId\":\"d582b9e9-b1c1-4f17-9279-0fe7333a****\",\"userId\":\"127067667954****\"},\"escalation\":{\"expression\":\"$Average>=800\",\"level\":P4,\"tag\":\"P4\",\"times\":1}",
            "RuleId": "d582b9e9-b1c1-4f17-9279-0f****_ResponseTime",
            "Escalation": {
                "Expression": "$Average>=800",
                "Times": 1,
                "Level": "P4"
            },
            "SendStatus": "0",
            "Product": "acs_ecs_dashboard",
            "MetricName": "cpu_total",
            "ContactSMSList": [],
            "RuleName": "CPU utilization",
            "ContactGroups": [
                "ECS_Group"
            ],
            "DingdingWebhookList": [],
            "InstanceId": "",
            "LevelChange": "P4->OK",
            "Dimensions": [
                {
                    "Value": "127067667954****",
                    "Key": "userId"
                },
                {
                    "Value": "i-abcdefgh12****",
                    "Key": "instanceId"
                }
            ],
            "ContactOnCallList": [],
            "ContactDingList": [],
            "EventName": "AlertOk",
            "ExtendedInfo": [
                {
                    "Value": "i-hp34y1eiszazu49y****",
                    "Name": "instanceId"
                },
                {
                    "Value": "12706****",
                    "Name": "userId"
                }
            ],
            "Namespace": "acs_ecs_dashboard",
            "AlertTime": 1610085521564,
            "GroupId": "7301****",
            "InstanceName": "portalHost",
            "WebhookList": [],
            "ContactMailList": [],
            "Level": "OK"
        }
    ],
    "RequestId": "6FCB1AB7-57F7-4DDA-B14E-6468FAFE79D9",
    "PageSize": 10,
    "PageNumber": 1,
    "Code": 200,
    "Success": true
}
```

## Error codes

|HTTP status code|Error code|Error message|Description|
|----------------|----------|-------------|-----------|
|404|ResourceNotFound|The specified resource is not found.|The error message returned because the specified resource is not found.|

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

