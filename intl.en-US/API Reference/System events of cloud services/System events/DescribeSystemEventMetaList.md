# DescribeSystemEventMetaList

Queries the meta information of system events.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeSystemEventMetaList&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeSystemEventMetaList|The operation that you want to perform. Set the value to DescribeSystemEventMetaList. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|Integer|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Data|Array of Resource|N/A|The detailed meta information. |
|Resource|N/A|N/A|N/A|
|EventType|String|Exception|The type of the system event. Valid values:

-   StatusNotification
-   Exception
-   Maintenance |
|Level|String|INFO|The level of the alert. Valid values:

-   CRITICAL
-   WARN
-   INFO |
|Name|String|SelectFailureRate|The name of the system event. |
|NameDesc|String|High query failure rate.|The description of the system event, in Chinese. |
|NameDesc.En|String|High query failure rate.|The description of the system event. |
|Product|String|ADS|The abbreviation of the service name. |
|Status|String|failed|The status of the system event. |
|StatusDesc|String|Operation Failed|The description of the event status. |
|Message|String|success|The returned message. |
|RequestId|String|A6582C8B-E67C-4A19-BC15-EAEFEBDC7995|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=DescribeSystemEventMetaList
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeSystemEventMetaListResponse>
          <RequestId>46350DCE-3399-473B-875F-1340DC97186C</RequestId>
          <Message>success</Message>
          <Data>
                <Resource>
                      <Status>Failed</Status>
                      <StatusDesc>OperationFailed</StatusDesc>
                      <NameDesc>The insertion failure rate is 10%.</NameDesc>
                      <NameDesc.En>InsertFailureRate</NameDesc.En>
                      <EventType>Exception</EventType>
                      <Product>ADS</Product>
                      <Level>CRITICAL</Level>
                      <Name>InsertFailureRate</Name>
                </Resource>
                <Resource>
                      <Status>Failed</Status>
                      <StatusDesc>OptionFailed</StatusDesc>
                      <NameDesc>The query failure rate is 10%.</NameDesc>
                      <NameDesc.En>SelectFailureRate</NameDesc.En>
                      <EventType>Exception</EventType>
                      <Product>ADS</Product>
                      <Level>CRITICAL</Level>
                      <Name>SelectFailureRate</Name>
                </Resource>
                <Resource>
                      <Status>Failed</Status>
                      <StatusDesc>Operation Failed</StatusDesc>
                      <NameDesc>The storage space usage is 80%.</NameDesc>
                      <NameDesc.En>StorageUsage</NameDesc.En>
                      <EventType>Maintenance</EventType>
                      <Product>ADS</Product>
                      <Level>CRITICAL</Level>
                      <Name>StorageUsage</Name>
                </Resource>
                <Resource>
                      <Status>EightyPercentQuotaExceeded</Status>
                      <StatusDesc>The resource usage exceeds 80% of the quota.</StatusDesc>
                      <NameDesc>The resource usage exceeds 80% of the quota.</NameDesc>
                      <NameDesc.En>EightyPercentQuotaExceeded:Route</NameDesc.En>
                      <EventType>80%QuotaExceeded</EventType>
                      <Product>CEN</Product>
                      <Level>WARN</Level>
                      <Name>EightyPercentQuotaExceeded:Route</Name>
                </Resource>
                <Resource>
                      <Status>NinetyEightPercentQuotaExceeded</Status>
                      <StatusDesc>The resource usage exceeds 98% of the quota.</StatusDesc>
                      <NameDesc>The resource usage exceeds 98% of the quota.</NameDesc>
                      <NameDesc.En>NinetyEightPercentQuotaExceeded:Route</NameDesc.En>
                      <EventType>98%QuotaExceeded</EventType>
                      <Product>CEN</Product>
                      <Level>WARN</Level>
                      <Name>NinetyEightPercentQuotaExceeded:Route</Name>
                </Resource>
          </Data>
          <Code>200</Code>
          <Success>true</Success>
</DescribeSystemEventMetaListResponse>
```

`JSON` format

```
{
    "RequestId": "46350DCE-3399-473B-875F-1340DC97186C",
    "Message": "success",
    "Data": {
        "Resource": [
         {
                "Status": "Failed",
                "StatusDesc": "OperationFailed",
                "NameDesc": "The insertion failure rate is 10%.",
                "NameDesc.En": "InsertFailureRate",
                "EventType": "Exception",
                "Product": "ADS",
                "Level": "CRITICAL",
                "Name": "InsertFailureRate"
            },
            {
                "Status": "Failed",
                "StatusDesc": "OptionFailed",
                "NameDesc": "The query failure rate is 10%.",
                "NameDesc.En": "SelectFailureRate",
                "EventType": "Exception",
                "Product": "ADS",
                "Level": "CRITICAL",
                "Name": "SelectFailureRate"
            },
            {
                "Status": "Failed",
                "StatusDesc": "Operation Failed",
                "NameDesc": "The storage space usage is 80%.",
                "NameDesc.En": "StorageUsage",
                "EventType": "Maintenance",
                "Product": "ADS",
                "Level": "CRITICAL",
                "Name": "StorageUsage"
            },
            {
                "Status": "EightyPercentQuotaExceeded",
                "StatusDesc": "The resource usage exceeds 80% of the quota.",
                "NameDesc": "The resource usage exceeds 80% of the quota.",
                "NameDesc.En": "EightyPercentQuotaExceeded:Route",
                "EventType": "80%QuotaExceeded",
                "Product": "CEN",
                "Level": "WARN",
                "Name": "EightyPercentQuotaExceeded:Route"
            },
            {
                "Status": "NinetyEightPercentQuotaExceeded",
                "StatusDesc": "The resource usage exceeds 98% of the quota.",
                "NameDesc": "The resource usage exceeds 98% of the quota.",
                "NameDesc.En": "NinetyEightPercentQuotaExceeded:Route",
                "EventType": "98%QuotaExceeded",
                "Product": "CEN",
                "Level": "WARN",
                "Name": "NinetyEightPercentQuotaExceeded:Route"
            }
        ]
    },
    "Code": "200",
    "Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

