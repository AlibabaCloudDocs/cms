# DescribeExporterOutputList

Queries configuration sets for exporting monitoring data.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeExporterOutputList&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeExporterOutputList|The operation that you want to perform. Set the value to **DescribeExporterOutputList**. |
|PageNumber|Integer|No|1|The number of the page to return. Default value: 1. |
|PageSize|Integer|No|10|The number of entries to return on each page. Default value: 10. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. Other status codes indicate that the call failed. |
|Datapoints|Array| |The configuration sets for exporting monitoring data. |
|Datapoint| | | |
|ConfigJson|Struct| |The JSON object that contains the detailed information about the destination to which the monitoring data is exported. |
|ak|String|LTAIpY33\*\*\*\*\*\*\*\*|The AccessKey ID. |
|as|String|TxHwuJ8yAb3AULcnny\*\*\*\*\*\*|The AccessKey secret. |
|endpoint|String|http://cn-qingdao-share.log.aliyuncs.com|The endpoint of Log Service to which the monitoring data is exported. |
|logstore|String|monitorlogstore|The Log Service Logstore to which the monitoring data is exported. |
|project|String|exporter|The Log Service project to which the monitoring data is exported. |
|CreateTime|Long|1584016495498|The UNIX timestamp when the configuration set was created. |
|DestName|String|exporterOut|The name of the configuration set. |
|DestType|String|SLS|The service to which the monitoring data is exported.

**Note:** Only Log Service is supported. More services will be supported in the future. |
|Message|String|success|The returned message. |
|PageNumber|Integer|1|The page number of the returned page. |
|RequestId|String|0E657631-CD6C-4C24-9637-98D000B9272C|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   `true`: indicates a success.
-   `false`: indicates a failure. |
|Total|Integer|25|The total number of entries returned. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=DescribeExporterOutputList
&<Common request parameters>
```

Sample success responses

`XML` format

```
<RequestId>BB30C6D9-8D0D-442E-9484-C15BADE76A21</RequestId>
<PageNumber>1</PageNumber>
<Total>1</Total>
<Datapoints>
    <Datapoint>
        <DestType>SLS</DestType>
        <DestName>desctName1</DestName>
        <CreateTime>1584016495498</CreateTime>
        <ConfigJson>
            <endpoint>http://cn-qingdao-share.log.aliyuncs.com</endpoint>
            <as>TxHwuJ8yAb3AULcnny******</as>
            <project>exporter</project>
            <ak>LTAIpY33********</ak>
            <logstore>exporter</logstore>
        </ConfigJson>
    </Datapoint>
</Datapoints>
<Code>200</Code>
<Success>true</Success>
```

`JSON` format

```
{
    "RequestId": "BB30C6D9-8D0D-442E-9484-C15BADE76A21",
    "PageNumber": 1,
    "Total": 1,
    "Datapoints": {
        "Datapoint": [
            {
                "DestType": "SLS",
                "DestName": "desctName1",
                "CreateTime": 1584016495498,
                "ConfigJson": {
                    "endpoint": "http://cn-qingdao-share.log.aliyuncs.com",
                    "as": "TxHwuJ8yAb3AULcnny******",
                    "project": "exporter",
                    "ak": "LTAIpY33********",
                    "logstore": "exporter"
                }
            }
        ]
    },
    "Code": "200",
    "Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

