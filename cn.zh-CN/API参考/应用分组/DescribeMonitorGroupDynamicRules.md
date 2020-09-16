# DescribeMonitorGroupDynamicRules

调用DescribeMonitorGroupDynamicRules接口查询应用分组动态规则列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeMonitorGroupDynamicRules&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeMonitorGroupDynamicRules|要执行的操作，取值：DescribeMonitorGroupDynamicRules。 |
|GroupId|Long|是|123456|应用分组ID。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|Integer|200|状态码。

 **说明：** 200表示成功。 |
|Message|String|The Request is not authorization.|错误信息。 |
|RequestId|String|2170B94A-1576-4D65-900E-2093037CDAF3|请求ID。 |
|Resource|Array of Resource| |关联资源。 |
|Resource| | | |
|Category|String|ecs|产品名称。 |
|FilterRelation|String|and|筛选条件。 |
|Filters|Array of Filter| |规则。 |
|Filter| | | |
|Function|String|contains|计算方法。取值：

 -   contains：包含。
-   startWith：前缀。
-   endWith：后缀。 |
|Name|String|hostName|待检查的字段名称。 |
|Value|String|aaa|动态规则值。 |
|GroupId|Long|12345|应用分组ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeMonitorGroupDynamicRules
&GroupId=123456
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeMonitorGroupDynamicRulesResponse>
      <Resource>
            <Resource>
                  <Filters>
                        <Filter>
                              <Name>hostName</Name>
                              <Value>aaa</Value>
                              <Function>contains</Function>
                        </Filter>
                  </Filters>
                  <Category>ecs</Category>
                  <FilterRelation>and</FilterRelation>
            </Resource>
      </Resource>
      <RequestId>2170B94A-1576-4D65-900E-2093037CDAF3</RequestId>
      <Success>true</Success>
      <Code>200</Code>
</DescribeMonitorGroupDynamicRulesResponse>
```

`JSON` 格式

```
{
  "Resource": {
    "Resource": [
      {
        "Filters": {
          "Filter": [
            {
              "Name": "hostName",
              "Value": "aaa",
              "Function": "contains"
            }
          ]
        },
        "Category": "ecs",
        "FilterRelation": "and"
      }
    ]
  },
  "RequestId": "2170B94A-1576-4D65-900E-2093037CDAF3",
  "Success": true,
  "Code": 200
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

