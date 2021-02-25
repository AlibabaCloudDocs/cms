# PutEventRule

调用PutEventRule接口创建或修改事件的报警规则。

如果报警规则名称不存在，则创建新的报警规则；如果报警规则名称存在，则修改已有报警规则。

本文将提供一个示例，为云服务`ecs`创建一条事件报警规则`myRuleName`。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=PutEventRule&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|PutEventRule|要执行的操作，取值：PutEventRule。 |
|EventPattern.N.Product|String|是|ecs|云服务类型。N的取值范围：1~50。

 **说明：** 关于事件报警规则支持的云服务，请参见[DescribeSystemEventMetaList](~~114972~~)。 |
|RuleName|String|是|myRuleName|事件报警规则名称。 |
|GroupId|String|否|7378\*\*\*\*|事件报警规则所属的应用分组ID。 |
|EventType|String|否|SYSTEM|事件报警规则的类型。取值：

 -   SYSTEM：系统事件。
-   CUSTOM：自定义事件。 |
|Description|String|否|事件报警测试|事件报警规则的描述。 |
|State|String|否|ENABLED|事件报警规则的状态。取值：

 -   ENABLED：启用。
-   DISABLED：禁用。 |
|EventPattern.N.NameList.N|RepeatList|否|Agent\_Status\_Stopped|事件报警规则的名称。N的取值范围：1~50。 |
|EventPattern.N.StatusList.N|RepeatList|否|Failed|事件报警规则的状态。N的取值范围：1~50。 |
|EventPattern.N.LevelList.N|RepeatList|否|CRITICAL|事件报警规则的等级。N的取值范围：1~50。取值：

 -   CRITICAL：严重。
-   WARN：警告。
-   INFO：信息。
-   \*：所有等级。 |
|EventPattern.N.EventTypeList.N|RepeatList|否|Exception|事件报警规则的类型。N的取值范围：1~50。取值：

 -   StatusNotification：故障通知。
-   Exception：异常。
-   Maintenance：运维。
-   \*：无限制。 |

关于公共请求参数的详情，请参见[公共参数](~~199331~~)。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|0B47C47B-E68A-4429-BB23-370E91889C7D|请求ID。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|Data|String|1|创建或修改事件报警规则时，返回影响的行数。 |
|Message|String|The Request is not authorization.|错误信息。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=PutEventRule
&EventPattern.1.Product=ecs
&RuleName=myRuleName
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<PutEventRuleResponse>
		  <RequestId>0B47C47B-E68A-4429-BB23-370E91889C7D</RequestId>
		  <Data>1</Data>
		  <Code>200</Code>
		  <Success>true</Success>
</PutEventRuleResponse>
```

`JSON`格式

```
{
	"RequestId": "0B47C47B-E68A-4429-BB23-370E91889C7D",
	"Data": "1",
	"Code": "200",
	"Success": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

