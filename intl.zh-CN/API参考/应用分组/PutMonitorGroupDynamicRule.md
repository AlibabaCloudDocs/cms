# PutMonitorGroupDynamicRule

调用PutMonitorGroupDynamicRule接口为应用分组创建或修改动态报警规则。满足报警规则的资源自动添加到该应用分组中。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=PutMonitorGroupDynamicRule&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|PutMonitorGroupDynamicRule|要执行的操作，取值：PutMonitorGroupDynamicRule。 |
|GroupId|Long|是|123456|应用分组ID。 |
|GroupRules.N.Category|String|是|ecs|动态报警规则的云服务类型。N的取值范围：1~3。取值：

 -   ecs：云服务器。
-   rds：关系型数据库。
-   slb：负载均衡。 |
|GroupRules.N.FilterRelation|String|是|and|动态报警规则的组合条件。N的取值范围：1~3。取值：

 -   and：满足所有报警规则的实例才会自动添加到应用分组。
-   or：满足任意报警规则的实例都会自动添加到应用分组。 |
|GroupRules.N.Filters.N.Function|String|是|contains|实例的过滤条件。N的取值范围：1~3。取值：

 -   contains：包含关系。
-   startWith：前缀。
-   endWith：后缀。 |
|GroupRules.N.Filters.N.Name|String|是|hostName|实例名称。N的取值范围：1~3。

 实例匹配的字段名称目前仅支持主机名：hostName。 |
|GroupRules.N.Filters.N.Value|String|是|nginx|满足报警条件的值。N的取值范围：1~3。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|3E73F1AB-D195-438A-BCA7-2F4355789C58|请求ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|Code|Integer|200|状态码。

 **说明：** 200表示成功。 |
|Message|String|The X.509 certificate or cms access key ID provided does not exist in our records.|错误信息。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=PutMonitorGroupDynamicRule
&GroupId=123456
&GroupRules.1.Category=ecs
&GroupRules.1.FilterRelation=and
&GroupRules.1.Filters.1.Function=contains
&GroupRules.1.Filters.1.1ame=hostName
&GroupRules.1.Filters.1.Value=nginx
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<PutMonitorGroupDynamicRuleResponse>
	  <RequestId>3E73F1AB-D195-438A-BCA7-2F4355789C58</RequestId>
	  <Success>true</Success>
	  <Code>200</Code>
</PutMonitorGroupDynamicRuleResponse>
```

`JSON` 格式

```
{
  "RequestId": "3E73F1AB-D195-438A-BCA7-2F4355789C58",
  "Success": true,
  "Code": 200
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

