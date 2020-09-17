# DescribeMonitorGroupNotifyPolicyList

调用DescribeMonitorGroupNotifyPolicyList接口查询应用分组的报警通知暂停策略列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeMonitorGroupNotifyPolicyList&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeMonitorGroupNotifyPolicyList|要执行的操作，取值：DescribeMonitorGroupNotifyPolicyList。 |
|PolicyType|String|是|PauseNotify|暂停通知类型。目前仅支持PauseNotify。 |
|RegionId|String|是|华东1（杭州）|目前仅支持3个地域。取值：

 -   华东1（杭州）
-   新加坡
-   日本（东京） |
|PageNumber|Integer|否|1|页码。默认值：1。 |
|PageSize|Integer|否|100|每页记录条数。默认值：10。 |
|GroupId|String|否|123\*\*\*\*|应用分组ID。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Message|String|The Request is not authorization.|错误信息。 |
|NotifyPolicyList|Array of NotifyPolicy| |暂停通知列表。 |
|NotifyPolicy| | | |
|EndTime|Long|1551761781273|结束时间。格式为Unix时间戳，即从1970年1月1日开始所经过的毫秒数。 |
|GroupId|String|123\*\*\*\*|应用分组ID。 |
|Id|String|123\*\*\*\*|暂停通知ID。 |
|StartTime|Long|1551761781273|开始时间。格式为Unix时间戳，即从1970年1月1日开始所经过的毫秒数。 |
|Type|String|PauseNotify|禁用类型。默认值：PauseNotify。 |
|RequestId|String|6072F026-C441-41A6-B114-35A1E8F8FDD3|请求ID。 |
|Success|String|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|Total|Integer|11|总记录条数。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeMonitorGroupNotifyPolicyList
&PolicyType=PauseNotify
&RegionId=华东1（杭州）
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeMonitorGroupNotifyPolicyListResponse>
    <NotifyPolicyList>
            <NotifyPolicy>
                  <Type>PauseNotify</Type>
                  <EndTime>1551763581273</EndTime>
                  <Id>123****</Id>
                  <StartTime>1551761781273</StartTime>
                  <GroupId>123****</GroupId>
            </NotifyPolicy>
      </NotifyPolicyList>
      <Success>true</Success>
      <Code>200</Code>
      <Total>1</Total>
</DescribeMonitorGroupNotifyPolicyListResponse>
```

`JSON` 格式

```
{
    "NotifyPolicyList": {
    "NotifyPolicy": [
      {
        "Type": "PauseNotify",
        "EndTime": 1551763581273,
        "Id": "123****",
        "StartTime": 1551761781273,
        "GroupId": "123****"
      }
    ]
  },
  "Success": true,
  "Code": "200",
  "Total": 1
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

