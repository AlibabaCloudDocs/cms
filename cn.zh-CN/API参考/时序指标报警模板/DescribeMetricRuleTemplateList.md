# DescribeMetricRuleTemplateList

调用DescribeMetricRuleTemplateList接口查询报警模板列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeMetricRuleTemplateList&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeMetricRuleTemplateList|要执行的操作，取值：DescribeMetricRuleTemplateList。 |
|Name|String|否|ECS\_Template1|报警模板名称。 |
|Keyword|String|否|ECS|按照报警模板名称模糊搜索。 |
|TemplateId|Long|否|12345|报警模板ID。 |
|PageNumber|Long|否|1|页码。默认值：1。 |
|PageSize|Long|否|10|每页显示模板的记录条数。 |
|History|Boolean|否|false|是否显示报警模板应用到应用分组的历史记录。取值：

 -   true：显示。
-   false（默认值）：不显示。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|Integer|200|状态码。

 **说明：** 200表示成功。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|Message|String|The Request is not authorization.|错误信息。 |
|Total|Long|11|总记录条数。 |
|RequestId|String|1A1B405A-B877-4A27-9922-471F080E4985|请求ID。 |
|Templates|Array of Template| |报警模板列表的数据。 |
|Template| | | |
|ApplyHistories|Array of ApplyHistory| |报警模板应用到应用分组的历史记录。 |
|ApplyHistory| | | |
|ApplyTime|Long|1543459583000|报警模板应用到应用分组的时间。 |
|GroupId|Long|12345|应用分组ID。 |
|GroupName|String|ECS\_Group|应用分组名称。 |
|Description|String|ECS的CPU使用率|报警模板详情。 |
|GmtCreate|Long|1543302440000|创建报警模板的时间戳。 |
|GmtModified|Long|1543302440000|修改报警模板的时间戳。 |
|Name|String|ECS\_Template1|报警模板名称。 |
|RestVersion|Long|0|报警模板版本。默认值：0。 |
|TemplateId|Long|12345|报警模板ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeMetricRuleTemplateList
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeMetricRuleTemplateListResponse>
      <RequestId>03AE5FA9-8CB2-4B5B-8306-1BBBF012A1A7</RequestId>
      <Templates>
            <Template>
                  <RestVersion>0</RestVersion>
                  <Name>newtemplate_1</Name>
                  <Description>ECS的CPU使用率</Description>
                  <GmtCreate>1543302440000</GmtCreate>
                  <GmtModified>1543302440000</GmtModified>
                  <TemplateId>32</TemplateId>
            </Template>
            <Template>
                  <RestVersion>0</RestVersion>
                  <Name>newtemplate_2</Name>
                  <Description></Description>
                  <GmtCreate>1543307344000</GmtCreate>
                  <GmtModified>1543307344000</GmtModified>
                  <TemplateId>42</TemplateId>
            </Template>
      </Templates>
      <Success>true</Success>
      <Code>200</Code>
      <Total>65</Total>
</DescribeMetricRuleTemplateListResponse>
```

`JSON` 格式

```
{
  "RequestId": "03AE5FA9-8CB2-4B5B-8306-1BBBF012A1A7",
  "Templates": {
    "Template": [
      {
        "RestVersion": 0,
        "Name": "newtemplate_1",
        "Description": "ECS的CPU使用率",
        "GmtCreate": 1543302440000,
        "GmtModified": 1543302440000,
        "TemplateId": 32
      },
      {
        "RestVersion": 0,
        "Name": "newtemplate_2",
        "Description": "",
        "GmtCreate": 1543307344000,
        "GmtModified": 1543307344000,
        "TemplateId": 42
      }
    ]
  },
  "Success": true,
  "Code": 200,
  "Total": 65
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

