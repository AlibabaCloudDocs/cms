# EnableActiveMetricRule

调用EnableActiveMetricRule接口启用一键报警规则。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=EnableActiveMetricRule&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|EnableActiveMetricRule|要执行的操作，取值：EnableActiveMetricRule。 |
|Product|String|是|ecs|支持一键报警规则的云服务名称。取值：

 -   ecs：云服务器ECS。
-   rds：云数据库RDS版）
-   slb：负载均衡。
-   redis\_standard：云数据库Redis标准版。
-   redis\_sharding：云数据库Redis集群版。
-   redis\_splitrw：云数据库Redis读写分离版。
-   mongodb：云数据库MongoDB版（副本集）。
-   mongodb\_sharding：云数据库MongoDB版（分片集群）。
-   hbase：云数据库HBase版。
-   elasticsearch：Elasticsearch。
-   opensearch：OpenSearch。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Message|String|The Request is not authorization.|错误信息。 |
|RequestId|String|F82E6667-7811-4BA0-842F-5B2DC42BBAAD|请求ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=EnableActiveMetricRule
&Product=ecs
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<EnableActiveMetricRuleResponse>
      <Code>200</Code>
      <Success>true</Success>
      <RequestId>55850888-9CCE-4FD5-B949-5F8947D63929</RequestId>
</EnableActiveMetricRuleResponse>
```

`JSON` 格式

```
{
  "Code": "200",
  "Success": true,
  "RequestId": "55850888-9CCE-4FD5-B949-5F8947D63929"
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

