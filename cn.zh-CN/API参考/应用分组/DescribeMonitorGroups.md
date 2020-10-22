# DescribeMonitorGroups

调用DescribeMonitorGroups接口查询应用分组列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeMonitorGroups&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeMonitorGroups|要执行的操作，取值：DescribeMonitorGroups。 |
|GroupName|String|否|demo|应用分组名称。 |
|Keyword|String|否|test|搜索关键字。 |
|PageSize|Integer|否|10|分页大小。默认值：10。 |
|PageNumber|Integer|否|1|分页页码。默认值：1。 |
|InstanceId|String|否|i-abcdefgh12\*\*\*\*|资源实例ID。查询指定实例所在的应用分组。 |
|SelectContactGroups|Boolean|否|true|返回结果中是否需要包含报警联系人组。取值：

 -   true：是。
-   false：否。 |
|IncludeTemplateHistory|Boolean|否|true|查询结果是否包含已应用到应用分组的报警模板历史。取值：

 -   true：是。
-   false：否。 |
|Tag.N.Key|String|否|testKey1|标签键。N的取值范围：1~5。 |
|Tag.N.Value|String|否|testValue1|标签值。N的取值范围：1~5。 |
|Type|String|否|custom|应用分组类型。取值：

 -   custom：自建的应用分组。
-   ehpc\_cluster：EHPC集群同步的应用分组。
-   kubernetes：Kubernetes同步的应用分组。 |
|DynamicTagRuleId|String|否|055995c1-4625-4dc0-8338-\*\*\*\*\*\*376950|智能标签规则ID。 |
|GroupId|String|否|123\*\*\*\*|应用分组ID。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|31BC7201-00F2-47B2-B7B9-6A173076ACE8|请求ID。 |
|Message|String|The Request is not authorization.|错误信息。 |
|PageNumber|Integer|1|应用分组列表的页码。 |
|PageSize|Integer|10|分页查询时设置的每页行数。 |
|Code|Integer|200|状态码。

 **说明：** 200表示成功。 |
|Resources|Array of Resource| |关联资源。 |
|Resource| | | |
|BindUrl|String|http://aliyun.com|从容器服务Kubernetes版同步过来的URL地址。 |
|ContactGroups|Array of ContactGroup| |报警联系组。 |
|ContactGroup| | | |
|Name|String|ECS\_Group|报警联系组名称。 |
|DynamicTagRuleId|String|055995c1-4625-4dc0-8338-\*\*\*\*\*\*376950|智能标签规则ID。 |
|GmtCreate|Long|1489043796000|创建时间。

 格式为Unix时间戳，即从1970年1月1日开始所经过的毫秒数。 |
|GmtModified|Long|1525183537000|修改时间。

 格式为Unix时间戳，即从1970年1月1日开始所经过的毫秒数。 |
|GroupFounderTagKey|String|portalGroup|创建者的标签键。

 **说明：** 如果应用分组通过智能标签同步创建，则该参数表示应用分组同步创建的标签键。 |
|GroupFounderTagValue|String|portalJP|创建者的标签值。

 **说明：** 如果应用分组通过智能标签同步创建，则该参数表示应用分组同步创建的标签值。 |
|GroupId|Long|12345|应用分组ID。 |
|GroupName|String|demo|应用分组名称。 |
|ServiceId|String|49\*\*\*\*|阿里云内部服务ID。 |
|Tags|Array of Tag| |应用分组绑定的标签列表。 |
|Tag| | | |
|Key|String|tagKey1|标签键。 |
|Value|String|tagValue1|标签值。 |
|TemplateIds|List|123|应用分组应用过的报警模板。

 **说明：** 如果IncludeTemplateHistory设置为true，则返回结果会显示该字段。 |
|Type|String|custom|应用分组类型。取值：

 -   custom：自建的应用分组。
-   ehpc\_cluster：EHPC集群同步的应用分组。
-   kubernetes：Kubernetes同步的应用分组。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|Total|Integer|10|总记录条数。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeMonitorGroups
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeMonitorGroupsResponse>
		  <PageNumber>1</PageNumber>
		  <PageSize>10</PageSize>
		  <RequestId>31BC7201-00F2-47B2-B7B9-6A173076ACE8</RequestId>
		  <Success>true</Success>
		  <Code>200</Code>
		  <Total>1</Total>
		  <Resources>
			    <Resource>
				      <GroupName>demo</GroupName>
				      <Type>custom</Type>
				      <ContactGroups>
					        <ContactGroup>
						          <Name>ECS_Group</Name>
					        </ContactGroup>
				      </ContactGroups>
				      <ServiceId>49****</ServiceId>
				      <GmtCreate>1489043796000</GmtCreate>
				      <GmtModified>1525183537000</GmtModified>
				      <GroupId>123****</GroupId>
				      <Tags>
					        <Tag>
						          <Value>tagValue1</Value>
						          <Key>tagKey1</Key>
					        </Tag>
				      </Tags>
				      <TemplateIds></TemplateIds>
			    </Resource>
		  </Resources>
</DescribeMonitorGroupsResponse>
```

`JSON` 格式

```
{
    "PageNumber": 1,
    "PageSize": 10,
    "RequestId": "31BC7201-00F2-47B2-B7B9-6A173076ACE8",
    "Success": true,
    "Code": 200,
    "Total": 1,
    "Resources": {
        "Resource": [
            {
                "GroupName": "demo",
                "Type": "custom",
                "ContactGroups": {
                    "ContactGroup": [
                        {
                            "Name": "ECS_Group"
                        }
                    ]
                },
                "ServiceId": "49****",
                "GmtCreate": "1489043796000",
                "GmtModified": "1525183537000",
                "GroupId": "123****",
                "Tags": {
					"Tag": [
						{
							"Value": "tagValue1",
							"Key": "tagKey1"
						}
					]
				},
                "TemplateIds": {
					"TemplateId": []
				}
            }
        ]
    }
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

