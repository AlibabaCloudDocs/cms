# DescribeProjectMeta

调用DescribeProjectMeta接口查询云监控支持的时序类监控项产品列表。

获取接入的云产品信息，包括产品的描述信息、Namespace和标签。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeProjectMeta&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeProjectMeta|要执行的操作，取值：DescribeProjectMeta。 |
|Labels|String|否|\[\{"name":"product","value":"ECS"\}\]|标签。根据标签过滤，标签为每个报警增加特殊标记。

 目前仅支持按照产品过滤，即`name`为`product`的过滤方式，例如：\{"name":"product","value":"ECS"\}。

 **说明：** 对于阿里云中云监控控制台的特殊标签，不建议您使用。 |
|PageNumber|Integer|否|1|页码。默认值：1。 |
|PageSize|Integer|否|30|分页大小。默认值：30。

 **说明：** 目前阿里云未限制该参数，如果您需要获取所有结果，则将分页大小设置为较大的值即可。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Message|String|The Request is not authorization.|错误信息。 |
|PageNumber|String|1|页码。 |
|PageSize|String|5|分页大小。 |
|RequestId|String|4C2061B2-3B1B-43BF-A4A4-C53426F479C0|请求ID。 |
|Resources|Array| |云产品信息。 |
|Resource| | | |
|Description|String|CDN|描述信息。 |
|Labels|String|\[\{"groupFlag":true\}\]|标签。根据标签过滤，标签为每个报警增加特殊标记。

 例如：报警所属产品的规格，是否能设置告警，格式：`[{"name":"标签名","value":"标签值"}、{"name":"标签名","value":"标签值"}]​`。常用的标签如下：

 -   alertUnit：报警的单位。

为了避免原始上报数据的单位过小，而导致告警规则输入的值过大而增加的`alertUnit`标签，目前主要应用于云监控控制台。

-   minAlertPeriod：最小上报周期。上报监控数据的时间间隔，通常为1分钟。
-   metricCategory：产品的规格。例如： kvstore\_sharding。

部分阿里云产品分不同规格，定义在同一个namespace中，用该参数进行区分。

-   is\_alarm：能否设置告警规则。

对于阿里云中云监控控制台的特殊标签，不建议您使用。 |
|Namespace|String|acs\_cdn|命名空间，用于区分产品。格式：`acs_产品缩写`，详情请参见[云产品监控项](~~163515~~)。 |
|Success|Boolean|true|操作是否成功。true表示成功，false表示失败。 |
|Total|String|12|总记录条数。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeProjectMeta
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeProjectMeta>
		  <PageNumber>1</PageNumber>
		  <PageSize>5</PageSize>
		  <RequestId>4C2061B2-3B1B-43BF-A4A4-C53426F479C0</RequestId>
		  <Success>true</Success>
		  <Code>200</Code>
		  <Total>12</Total>
		  <Resources>
			    <Resource>
				      <Description>分析型数据库</Description>
				      <Labels>[{"name":"product","value":"ADS"},{"name":"productCategory","value":"ads"},{"name":"groupFlag","value":"true"}]</Labels>
				      <Namespace>acs_ads</Namespace>
			    </Resource>
			    <Resource>
				      <Description>智能推荐</Description>
				      <Labels>[{"name":"product","value":"AIRec"},{"name":"productCategory","value":"airec"},{"name":"groupFlag","value":"true"}]</Labels>
				      <Namespace>acs_airec</Namespace>
			    </Resource>
			    <Resource>
				      <Description>API网关</Description>
				      <Labels>[{"name":"product","value":"APIGateway"},{"name":"productCategory","value":"apigateway"},{"name":"groupFlag","value":"true"}]</Labels>
				      <Namespace>acs_apigateway_dashboard</Namespace>
			    </Resource>
			    <Resource>
				      <Description>CDN</Description>
				      <Labels>[{"name":"product","value":"CDN"},{"name":"productCategory","value":"cdn"},{"name":"groupFlag","value":"true"}]</Labels>
				      <Namespace>acs_cdn</Namespace>
			    </Resource>
			    <Resource>
				      <Description>云企业网</Description>
				      <Labels>[{"name":"product","value":"CEN"},{"name":"productCategory","value":"cen,cen_flow,cen_vbr"},{"name":"groupFlag","value":"true"}]</Labels>
				      <Namespace>acs_cen</Namespace>
			    </Resource>
		  </Resources>
</DescribeProjectMeta>
```

`JSON` 格式

```
{
  "PageNumber": 1,
  "PageSize": 5,
  "RequestId": "4C2061B2-3B1B-43BF-A4A4-C53426F479C0",
  "Success": true,
  "Code": 200,
  "Total": 12,
  "Resources": {
    "Resource": [
      {
        "Description": "分析型数据库",
        "Labels": "[{\"name\":\"product\",\"value\":\"ADS\"},{\"name\":\"productCategory\",\"value\":\"ads\"},{\"name\":\"groupFlag\",\"value\":\"true\"}]",
        "Namespace": "acs_ads"
      },
      {
        "Description": "智能推荐",
        "Labels": "[{\"name\":\"product\",\"value\":\"AIRec\"},{\"name\":\"productCategory\",\"value\":\"airec\"},{\"name\":\"groupFlag\",\"value\":\"true\"}]",
        "Namespace": "acs_airec"
      },
      {
        "Description": "API网关",
        "Labels": "[{\"name\":\"product\",\"value\":\"APIGateway\"},{\"name\":\"productCategory\",\"value\":\"apigateway\"},{\"name\":\"groupFlag\",\"value\":\"true\"}]",
        "Namespace": "acs_apigateway_dashboard"
      },
      {
        "Description": "CDN",
        "Labels": "[{\"name\":\"product\",\"value\":\"CDN\"},{\"name\":\"productCategory\",\"value\":\"cdn\"},{\"name\":\"groupFlag\",\"value\":\"true\"}]",
        "Namespace": "acs_cdn"
      },
      {
        "Description": "云企业网",
        "Labels": "[{\"name\":\"product\",\"value\":\"CEN\"},{\"name\":\"productCategory\",\"value\":\"cen,cen_flow,cen_vbr\"},{\"name\":\"groupFlag\",\"value\":\"true\"}]",
        "Namespace": "acs_cen"
      }
    ]
  }
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

