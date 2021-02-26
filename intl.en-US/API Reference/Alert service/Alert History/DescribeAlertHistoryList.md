# DescribeAlertHistoryList

Queries historical alerts.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeAlertHistoryList&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeAlertHistoryList|The operation that you want to perform. Set the value to DescribeAlertHistoryList. |
|RuleId|String|No|aaaabbb123|The ID of the alert rule. |
|RuleName|String|No|My alert rule|The name of the alert rule. |
|Namespace|String|No|acs\_ecs\_dashboard|The namespace of the service.

**Note:** For more information, see [DescribeMetricMetaList](~~98846~~) or [Appendix 1: Metrics](~~163515~~). |
|MetricName|String|No|cpu\_total|The name of the metric.

**Note:** For more information, see [DescribeMetricMetaList](~~98846~~) or [Appendix 1: Metrics](~~163515~~). |
|GroupId|String|No|123456|The ID of the application group. |
|Status|String|No|Status|The status of the mute period. Valid values:

-   2: indicates that alerts are muted and are not triggered within the period, even if the condition specified in the alert rule is met.
-   0: indicates that the alert is triggered or cleared. |
|State|String|No|ALARM|The alert status. Valid values:

-   ALARM: indicates that alerts are triggered.
-   OK: indicates that no alerts are triggered. |
|Ascending|Boolean|No|true|The order of alerts. Valid values:

-   true: the reverse chronological order.
-   false: the chronological order.

Default value: true. |
|StartTime|String|No|1554085998000|The beginning of the time range for the query.

Set the value to a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|EndTime|String|No|1554085998000|The end of the time range for the query.

Set the value to a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|PageSize|Integer|No|10|The number of entries to return on each page. |
|Page|Integer|No|1|The number of the page to return. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|189B35DD-68BA-43CE-A66A-57F0BE12C885|The ID of the request. |
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Success|Boolean|true|Indicates whether the call was successful. The value true indicates a success. The value false indicates a failure. |
|Total|String|2|The total number of entries returned. |
|AlarmHistoryList|Array| |The details of historical alerts. |
|AlarmHistory| | | |
|AlertTime|Long|1554105040000|The time when the alert was triggered. |
|ContactALIIMs|List|My TradeManager|The TradeManager accounts to which the alert notification was sent. |
|ContactGroups|List|The group of alert contacts|The alert groups to which the alert notification was sent. |
|ContactMails|List|xxx@aliyun.com|The email addresses to which the alert notification was sent. |
|ContactSmses|List|1333333\*\*\*\*|The mobile phone numbers to which the alert notification was sent. |
|Contacts|List|My alert contacts|The alert contacts to which the alert notification was sent. |
|Dimensions|String|\{"instanceId":"i-2zebwilv3xfdg1\*\*\*\*"\}|The resources that are associated with the alert rule. |
|EvaluationCount|Integer|2|The consecutive number of times for which the metric value was measured before the alert was triggered. |
|Expression|String|$Average\>=1|The expression that defines the condition for triggering the alert. |
|GroupId|String|123456|The ID of the application group. |
|InstanceName|String|ali-186xxxx123456|The name of the instance. |
|LastTime|Long|347020693|The time when the status last changed. |
|Level|String|P3|The level of the alert. Valid values:


P4: The alert notification is delivered by using emails and DingTalk Chatbot. |
|MetricName|String|cpu\_total|The name of the metric.

**Note:** For more information, see [DescribeMetricMetaList](~~98846~~) or [Appendix 1: Metrics](~~163515~~). |
|Namespace|String|acs\_ecs\_dashboard|The namespace of the service.

**Note:** For more information, see [DescribeMetricMetaList](~~98846~~) or [Appendix 1: Metrics](~~163515~~). |
|RuleId|String|d97a65a7-70d2-4a8a-97bf-1a9147\*\*\*\*|The ID of the alert rule. |
|RuleName|String|My alert rule|The name of the alert rule. |
|State|String|ALARM|The alert status. Valid values:

-   ALARM: indicates that alerts are triggered.
-   OK: indicates that no alerts are triggered. |
|Status|Integer|2|The status of the mute period. Valid values:

-   2: indicates that alerts are muted and are not triggered within the period, even if the condition specified in the alert rule is met.
-   0: indicates that the alert is triggered or cleared. |
|Value|String|5.39|The threshold of the metric value for the alert to be triggered. |
|Webhooks|String|http://www.aliyun.com/webhook.html|The callback URL. |
|Message|String|The Request is not authorization.|The returned message. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=DescribeAlertHistoryList
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeAlertHistoryList>
      <AlarmHistoryList>
            <AlarmHistory>
                  <Value>4.41</Value>
                  <LastTime>881140083</LastTime>
                  <Webhooks></Webhooks>
                  <ContactSmses></ContactSmses>
                  <RuleName>test-auto-scaling-0001</RuleName>
                  <GroupId>123456</GroupId>
                  <AlertName>putNewAlarm_xxxxxx</AlertName>
                  <EvaluationCount>1</EvaluationCount>
                  <Status>2</Status>
                  <AlertState>ALARM</AlertState>
                  <MetricName>cpu_total#60</MetricName>
                  <ContactMails></ContactMails>
                  <AlertTime>1554986620000</AlertTime>
                  <Dimensions>{"instanceId":"i-2******3"}</Dimensions>
                  <RuleId>bfae2ca5b4e07d2c7278772eccda169808c7b****</RuleId>
                  <Contacts></Contacts>
                  <Namespace>acs_ecs</Namespace>
                  <ContactALIIMs></ContactALIIMs>
                  <ContactGroups></ContactGroups>
                  <Expression>$Average&gt;=1</Expression>
                  <Level>P3</Level>
                  <InstanceName></InstanceName>
            </AlarmHistory>
            <AlarmHistory>
                  <Value>2.13</Value>
                  <LastTime>760058</LastTime>
                  <Webhooks></Webhooks>
                  <ContactSmses></ContactSmses>
                  <RuleName>test-auto-scaling-0001</RuleName>
                  <GroupId>123456</GroupId>
                  <AlertName>putNewAlarm_us****</AlertName>
                  <EvaluationCount>1</EvaluationCount>
                  <Status>2</Status>
                  <AlertState>ALARM</AlertState>
                  <MetricName>cpu_total#60</MetricName>
                  <ContactMails></ContactMails>
                  <AlertTime>1554986620000</AlertTime>
                  <Dimensions>{"instanceId":"i-2z*****"}</Dimensions>
                  <RuleId>bfae2ca5b4e07d2c7278772eccda169808c7b****</RuleId>
                  <Contacts></Contacts>
                  <Namespace>acs_ecs</Namespace>
                  <ContactALIIMs></ContactALIIMs>
                  <ContactGroups></ContactGroups>
                  <Expression>$Average&gt;=1</Expression>
                  <Level>P3</Level>
                  <InstanceName></InstanceName>
            </AlarmHistory>
      </AlarmHistoryList>
      <RequestId>FEBE3561-166F-4DB2-BB59-020B26F30318</RequestId>
      <Success>true</Success>
      <Code>200</Code>
      <Total>102390</Total>
</DescribeAlertHistoryList>
```

`JSON` format

```
{
  "AlarmHistoryList": {
    "AlarmHistory": [
      {
        "Value": "4.41",
        "LastTime": 881140083,
        "Webhooks": "",
        "ContactSmses": {
          "ContactSms": []
        },
        "RuleName": "test-auto-scaling-0001",
        "GroupId": "123456",
        "AlertName": "putNewAlarm_xxxxxx",
        "EvaluationCount": 1,
        "Status": 2,
        "AlertState": "ALARM",
        "MetricName": "cpu_total#60",
        "ContactMails": {
          "ContactMail": []
        },
        "AlertTime": 1554986620000,
        "Dimensions": "{\"instanceId\":\"i-2******3\"}",
        "RuleId": "bfae2ca5b4e07d2c7278772eccda169808c7b****",
        "Contacts": {
          "Contact": []
        },
        "Namespace": "acs_ecs",
        "ContactALIIMs": {
          "ContactALIIM": []
        },
        "ContactGroups": {
          "ContactGroup": []
        },
        "Expression": "$Average>=1",
        "Level": "P3",
        "InstanceName": ""
      },
      {
        "Value": "2.13",
        "LastTime": 760058,
        "Webhooks": "",
        "ContactSmses": {
          "ContactSms": []
        },
        "RuleName": "test-auto-scaling-0001",
        "GroupId": "123456",
        "AlertName": "putNewAlarm_us****",
        "EvaluationCount": 1,
        "Status": 2,
        "AlertState": "ALARM",
        "MetricName": "cpu_total#60",
        "ContactMails": {
          "ContactMail": []
        },
        "AlertTime": 1554986620000,
        "Dimensions": "{\"instanceId\":\"i-2z*****\"}",
        "RuleId": "bfae2ca5b4e07d2c7278772eccda169808c7b****",
        "Contacts": {
          "Contact": []
        },
        "Namespace": "acs_ecs",
        "ContactALIIMs": {
          "ContactALIIM": []
        },
        "ContactGroups": {
          "ContactGroup": []
        },
        "Expression": "$Average>=1",
        "Level": "P3",
        "InstanceName": ""
      }
    ]
  },
  "RequestId": "FEBE3561-166F-4DB2-BB59-020B26F30318",
  "Success": true,
  "Code": "200",
  "Total": 102390
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

