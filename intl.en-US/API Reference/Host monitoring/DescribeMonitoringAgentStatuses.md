# DescribeMonitoringAgentStatuses

Queries the status of the Cloud Monitor agent.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeMonitoringAgentStatuses&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeMonitoringAgentStatuses|The operation that you want to perform. Set the value to DescribeMonitoringAgentStatuses. |
|InstanceIds|String|Yes|i-12345w55tr2rcpejp\*\*\*\*,i-23456w55tr2rcpejp\*\*\*\*|The ID of the instance. Separate multiple instance IDs with commas \(,\). |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Message|String|The Request is not authorization.|The returned message. |
|NodeStatusList|Array of NodeStatus|N/A|The status of the Cloud Monitor agent on the instances. |
|NodeStatus|N/A|N/A|N/A|
|AutoInstall|Boolean|true|Indicates whether automatic installation is enabled. Valid values:

-   true
-   false |
|InstanceId|String|i-123456w55tr2rcpejp\*\*\*\*|The ID of the instance. |
|Status|String|running|The status of the Cloud Monitor agent. Valid values:

-   running: The Cloud Monitor agent is running on the instance.
-   stopped: The Cloud Monitor agent is stopped on the instance.
-   installing: The Cloud Monitor agent is being installed on the instance.
-   install\_faild: The Cloud Monitor agent fails to be installed on the instance.
-   abnormal: The Cloud Monitor agent is not properly installed on the instance.
-   not\_installed: The Cloud Monitor agent is not installed on the instance. |
|RequestId|String|E9F4FA2A-54BE-4EF9-9D1D-1A0B1DC86B8D|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=DescribeMonitoringAgentStatuses
&InstanceIds=i-12345w55tr2rcpejp****,i-23456w55tr2rcpejp****
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeMonitoringAgentStatusesResponse>
      <NodeStatusList>
            <NodeStatus>
                  <Status>running</Status>
                  <InstanceId>i-123455cpejp****</InstanceId>
                  <AutoInstall>true</AutoInstall>
            </NodeStatus>
            <NodeStatus>
                  <Status>running</Status>
                  <InstanceId>i-123567kg04****</InstanceId>
                  <AutoInstall>true</AutoInstall>
            </NodeStatus>
      </NodeStatusList>
      <Success>true</Success>
      <Code>200</Code>
</DescribeMonitoringAgentStatusesResponse>
```

`JSON` format

```
{
    "NodeStatusList": {
        "NodeStatus": [
            {
                "Status": "running",
                "InstanceId": "i-123455cpejp****",
                "AutoInstall": true
            },
            {
                "Status": "running",
                "InstanceId": "i-123567kg04****",
                "AutoInstall": true
            }
        ]
    },
    "Success": true,
    "Code": 200
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

