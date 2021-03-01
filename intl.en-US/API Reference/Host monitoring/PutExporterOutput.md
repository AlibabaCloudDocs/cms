# PutExporterOutput

Creates or modifies a configuration set for exporting monitoring data.

**Note:** The monitoring data can be exported only to Log Service. More services will be supported in the future.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=PutExporterOutput&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|PutExporterOutput|The operation that you want to perform. Set the value to PutExporterOutput. |
|ConfigJson|String|Yes|\{ "endpoint": "http://cn-qingdao-share.log.aliyuncs.com", "project": "exporter", "logstore": "exporter","ak": "LTAIp\*\*\*\*\*\*\*", "userId": "17754\*\*\*\*\*\*\*\*", "as": "TxHwuJ8yAb3AU\*\*\*\*\*\*"\}|The configuration set for exporting monitoring data. It is a JSON object string. The string must includes the following fields:

-   endpoint: the endpoint of Log Service.
-   project: the Log Service project to which monitoring data is exported.
-   logstore: the Log Service Logstore to which the monitoring data is exported.
-   ak: the AccessKey ID.
-   as: the AccessKey secret. |
|DestName|String|Yes|exporterConfig|The name of the configuration set. |
|DestType|String|Yes|sls|The service to which the monitoring data is exported. |
|Desc|String|No|Export CPU metrics|The description of the configuration set. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Message|String|The Request is not authorization.|The returned message. |
|RequestId|String|6A5F022D-AC7C-460E-94AE-B9E75083D027|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. The value true indicates a success. The value false indicates a failure. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=PutExporterOutput
&ConfigJson={ "endpoint": "http://cn-qingdao-share.log.aliyuncs.com", "project": "exporter", "logstore": "exporter","ak": "LTAIp*******", "userId": "17754********", "as": "TxHwuJ8yAb3AU******"}
&DestName=exporterConfig
&DestType=sls
&<Common request parameters>
```

Sample success responses

`XML` format

```
<PutExporterOutput>
          <RequestId>E5DC60DD-2FDE-488F-942C-424FA3E18BF8</RequestId>
          <Code>200</Code>
          <Success>true</Success>
</PutExporterOutput>
```

`JSON` format

```
{
    "RequestId": "E5DC60DD-2FDE-488F-942C-424FA3E18BF8",
    "Code": "200",
    "Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

