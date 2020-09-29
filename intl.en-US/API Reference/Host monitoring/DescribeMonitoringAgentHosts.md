# DescribeMonitoringAgentHosts

Queries hosts with and without the Cloud Monitor agent installed.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeMonitoringAgentHosts&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeMonitoringAgentHosts|The operation that you want to perform. Set the value to DescribeMonitoringAgentHosts. |
|KeyWord|String|No|host1|The keyword that is used in fuzzy match. |
|HostName|String|No|hostNam1|The name of the host. |
|InstanceIds|String|No|i-a3d1q1pm2f9yr29e\*\*\*\*|The ID of the instance. |
|SerialNumbers|String|No|a1ab31a3-1234-40f2-9e95-c8caa8f0\*\*\*\*|The serial number of the host.

After the Cloud Monitor Agent is installed on a host, a globally unique serial number is generated. A host that is not provided by Alibaba Cloud has a serial number instead of an instance ID.

**Note:** This parameter can be used in exact search for any monitored hosts. |
|PageNumber|Integer|No|1|The number of the page to return. |
|PageSize|Integer|No|10|The number of entries to return on each page. Valid values:

-   10
-   20
-   50
-   100

**Note:** Alibaba Cloud does not limit the maximum value of this parameter. However, we recommend that you do not specify a large value to obtain all the instances on a page. If you specify a large value for this parameter, you may fail to obtain the instances due to a timeout error. |
|InstanceRegionId|String|No|cn-hangzhou|The region ID of the instance. |
|AliyunHost|Boolean|No|true|Specifies whether to query Elastic Compute Service \(ECS\) instances that are provided by Alibaba Cloud or to query hosts that are not provided by Alibaba Cloud. Default value: true. Valid values:

-   true: All the ECS instances that are provided by Alibaba Cloud are returned.
-   false: All the hosts that are not provided by Alibaba Cloud are returned. |
|Status|String|No|Running|The status of the hosts to query. Valid values:

-   Running: queries the hosts that are running.
-   Stopped: queries the hosts that are stopped, are not installed, or fail to be installed. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|63EEBB2A-9E51-41E4-9E83-5DE7F3B292E0|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |
|Total|Integer|10|The total number of the returned entries. |
|PageTotal|Integer|50|The total number of the returned pages. |
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Hosts|Array of Host|N/A|The information about the hosts. |
|Host|N/A|N/A|N/A|
|AgentVersion|String|3.4.6|The version of the Cloud Monitor agent. |
|AliUid|Long|123456789|The ID of the Alibaba Cloud account. |
|EipAddress|String|192.168.XX.XX|The elastic IP address \(EIP\) of the host. |
|EipId|String|eip-bp16i16k9gcezyfrp\*\*\*\*|The ID of the EIP. |
|HostName|String|hostIP|The name of the host. |
|InstanceId|String|i-a2d5q7pm3f9yr212\*\*\*\*|The ID of the instance. |
|InstanceTypeFamily|String|ecs.n4|The type of the ECS instance. |
|IpGroup|String|192.168.XX.XX|The IP address of the host.

**Note:** Multiple IP addresses are separated with commas \(,\). |
|NatIp|String|192.168.XX.XX|The IP address of the Network Address Translation \(NAT\) gateway. |
|NetworkType|String|vpc|The type of the network. |
|OperatingSystem|String|Linux|The operating system. |
|Region|String|cn-hangzhou|The ID of the region where the host resides. |
|SerialNumber|String|x12335-6cc8-4a22-9f21-1a00a719\*\*\*\*|The serial number of the host. A host that is not provided by Alibaba Cloud has a serial number instead of an instance ID.

**Note:** This parameter can be used in exact search for any monitored hosts. |
|isAliyunHost|Boolean|true|Indicates whether the host is provided by Alibaba Cloud. Valid values:

-   true
-   false |
|Message|String|The Request is not authorization.|The returned message. |
|PageNumber|Integer|1|The number of the returned page. Default value: 1 |
|PageSize|Integer|10|The number of entries returned on each page. Default value: 30. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=DescribeMonitoringAgentHosts
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeMonitoringAgentHostsResponse>
          <Hosts>
                <Host>
                      <OperatingSystem>Windows</OperatingSystem>
                      <SerialNumber>f0a434f2-632b-4588-95e6-202d4396****</SerialNumber>
                      <isAliyunHost>true</isAliyunHost>
                      <InstanceId>i-uf6hm9lnlzsarrc7****</InstanceId>
                      <AgentVersion>3.4.6</AgentVersion>
                      <NetworkType>vpc</NetworkType>
                      <InstanceTypeFamily>ecs.g6</InstanceTypeFamily>
                      <Region>cn-shanghai</Region>
                      <IpGroup>192.168.XX.XX,192.168.XX.XX</IpGroup>
                      <HostName>iZlzsarrc78****</HostName>
                      <AliUid>103201326074****</AliUid>
                </Host>
                <Host>
                      <OperatingSystem>Linux</OperatingSystem>
                      <SerialNumber>9c336dc5-1802-4db0-b7a0-2d46ad4f****</SerialNumber>
                      <isAliyunHost>true</isAliyunHost>
                      <InstanceId>i-uf6hn19s56zumk9w****</InstanceId>
                      <AgentVersion>3.4.4</AgentVersion>
                      <NetworkType>vpc</NetworkType>
                      <InstanceTypeFamily>ecs.g5</InstanceTypeFamily>
                      <Region>cn-shanghai</Region>
                      <IpGroup>192.168.XX.XX,192.168.XX.XX</IpGroup>
                      <HostName>launch-advisor-2019****</HostName>
                      <AliUid>103201326074****</AliUid>
                </Host>
          </Hosts>
          <PageSize>100</PageSize>
          <PageNumber>1</PageNumber>
          <PageTotal>1</PageTotal>
          <Total>5</Total>
          <Code>200</Code>
          <Success>true</Success>
</DescribeMonitoringAgentHostsResponse>
```

`JSON` format

```
{
    "Hosts": {
        "Host": [{
                "OperatingSystem": "Windows",
                "SerialNumber": "f0a434f2-632b-4588-95e6-202d4396****",
                "isAliyunHost": true,
                "InstanceId": "i-uf6hm9lnlzsarrc7****",
                "AgentVersion": "3.4.6",
                "NetworkType": "vpc",
                "InstanceTypeFamily": "ecs.g6",
                "Region": "cn-shanghai",
                "IpGroup": "192.168.XX.XX,192.168.XX.XX",
                "HostName": "iZlzsarrc78****",
                "AliUid": "103201326074****"
            },
            {
                "OperatingSystem": "Linux",
                "SerialNumber": "9c336dc5-1802-4db0-b7a0-2d46ad4f****",
                "isAliyunHost": true,
                "InstanceId": "i-uf6hn19s56zumk9w****",
                "AgentVersion": "3.4.4",
                "NetworkType": "vpc",
                "InstanceTypeFamily": "ecs.g5",
                "Region": "cn-shanghai",
                "IpGroup": "192.168.XX.XX,192.168.XX.XX",
                "HostName": "launch-advisor-2019****",
                "AliUid": "103201326074****"
            }
        ]
    },
    "PageSize": 100,
    "PageNumber": 1,
    "PageTotal": 1,
    "Total": 5,
    "Code": 200,
    "Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

