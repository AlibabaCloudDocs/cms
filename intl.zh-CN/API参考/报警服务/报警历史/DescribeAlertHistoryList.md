# DescribeAlertHistoryList

调用DescribeAlertHistoryList接口查询报警历史详情。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeAlertHistoryList&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAlertHistoryList|要执行的操作，取值：DescribeAlertHistoryList。 |
|RuleId|String|否|aaaabbb123|报警规则ID。 |
|RuleName|String|否|我的报警规则|报警规则名称。 |
|Namespace|String|否|acs\_ecs\_dashboard|产品的数据命名空间。

 **说明：** 详情请参见[DescribeMetricMetaList](~~98846~~)或[云产品监控项](~~163515~~)。 |
|MetricName|String|否|cpu\_total|监控项名称。

 **说明：** 详情请参见[DescribeMetricMetaList](~~98846~~)或[云产品监控项](~~163515~~)。 |
|GroupId|String|否|123456|应用分组ID。 |
|Status|String|否|Status|通道沉默状态。取值：

 -   2：通道沉默
-   0：报警或恢复 |
|State|String|否|ALARM|报警状态。取值：

 -   ALARM：报警状态
-   OK：正常状态 |
|Ascending|Boolean|否|true|时间排序。取值：

 -   true：表示时间倒序
-   false：表示时间正序

 默认值：true。 |
|StartTime|String|否|1554085998000|开始时间。

 格式为Unix时间戳，即从1970年1月1日开始所经过的毫秒数。 |
|EndTime|String|否|1554085998000|结束时间。

 格式为Unix时间戳，即从1970年1月1日开始所经过的毫秒数。 |
|PageSize|Integer|否|10|每页显示记录条数。 |
|Page|Integer|否|1|页码。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|189B35DD-68BA-43CE-A66A-57F0BE12C885|请求ID。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Success|Boolean|true|操作是否成功。true表示成功，false表示失败。 |
|Total|String|2|总记录条数。 |
|AlarmHistoryList|Array| |报警历史详情。 |
|AlarmHistory| | | |
|AlertTime|Long|1554105040000|发生报警的时间。 |
|ContactALIIMs|List|我的旺旺|旺旺报警通知。 |
|ContactGroups|List|报警通知联系组|报警联系人组。 |
|ContactMails|List|xxx@aliyun.com|邮件报警通知人。 |
|ContactSmses|List|1333333\*\*\*\*|短信报警联系方式，手机号码列表。 |
|Contacts|List|我的报警联系人|报警联系人。 |
|Dimensions|String|\{"instanceId":"i-2zebwilv3xfdg1\*\*\*\*"\}|关联的资源。 |
|EvaluationCount|Integer|2|报警重试次数。 |
|Expression|String|$Average\>=1|报警触发表达式。 |
|GroupId|String|123456|应用分组ID。 |
|InstanceName|String|ali-186xxxx123456|实例名称。 |
|LastTime|Long|347020693|最后一次状态改变的时间。 |
|Level|String|P3|报警级别。取值：

 
 P4：邮件、旺旺、钉钉机器人 |
|MetricName|String|cpu\_total|监控项名称。

 **说明：** 详情请参见[DescribeMetricMetaList](~~98846~~)或[云产品监控项](~~163515~~)。 |
|Namespace|String|acs\_ecs\_dashboard|产品的数据命名空间。

 **说明：** 详情请参见[DescribeMetricMetaList](~~98846~~)或[云产品监控项](~~163515~~)。 |
|RuleId|String|d97a65a7-70d2-4a8a-97bf-1a9147\*\*\*\*|报警规则ID。 |
|RuleName|String|我的报警|报警规则名称。 |
|State|String|ALARM|报警状态。取值：

 -   ALARM：报警状态
-   OK：正常状态 |
|Status|Integer|2|通道沉默状态。取值：

 -   2：通道沉默
-   0：报警或恢复 |
|Value|String|5.39|出现报警或恢复时的监控值。 |
|Webhooks|String|http://www.aliyun.com/webhook.html|URL回调地址。 |
|Message|String|The Request is not authorization.|错误信息。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeAlertHistoryList
&<公共请求参数>
```

正常返回示例

`XML` 格式

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

`JSON` 格式

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

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

