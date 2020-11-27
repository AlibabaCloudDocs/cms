# SendDryRunSystemEvent

Debugs a system event of an Alibaba Cloud resource.

This operation is used to test whether a system event can be triggered as expected. You can call this operation to simulate a system event and check whether an expected response is returned after an alert is triggered by the system event.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=SendDryRunSystemEvent&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|SendDryRunSystemEvent|The operation that you want to perform. Set the value to SendDryRunSystemEvent. |
|EventName|String|Yes|Agent\_Status\_Stopped|The name of the system event.

 **Note:** For more information, see [DescribeSystemEventMetaList](~~114972~~). |
|Product|String|Yes|ecs|The name of the cloud service.

 **Note:** For information about the system events supported by Cloud Monitor for Alibaba Cloud services, see [System events](~~167388~~). |
|GroupId|String|No|123456|The ID of the application group. |
|EventContent|String|No|\{"product":"CloudMonitor","resourceId":"acs:ecs:cn-hongkong:173651113438\*\*\*\*:instance/\{instanceId\}","level":"CRITICAL","instanceName":"instanceName","regionId":"cn-hangzhou","name":"Agent\_Status\_Stopped","content":\{"ipGroup":"0.0.0.0,0.0.0.1","tianjimonVersion":"1.2.11"\},"status":"stopped"\}|The content of the system event.

 **Note:** The value of this parameter is a JSON object. We recommend that you include the `product`, `resourceId`, and `regionId` fields in the JSON object. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|486029C9-53E1-44B4-85A8-16A571A043FD|The ID of the request. |
|Success|String|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |
|Code|String|200|The HTTP status code.

 **Note:** The status code 200 indicates that the call was successful. |
|Message|String|success|The returned message. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=SendDryRunSystemEvent
&EventName=Agent_Status_Stopped
&Product=ecs
&<Common request parameters>
```

Sample success responses

`XML` format

```
<SendDryRunSystemEventResponse>
	  <Message>success</Message>
	  <RequestId>590FB642-5FFE-4AE0-883B-E1323DD20541</RequestId>
	  <Code>200</Code>
	  <Success>true</Success>
</SendDryRunSystemEventResponse>
```

`JSON` format

```
{
  "Message": "success",
  "RequestId": "590FB642-5FFE-4AE0-883B-E1323DD20541",
  "Code": "200",
  "Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

