# Common parameters

This topic describes common parameters, including common request parameters and common response parameters.

## Sample common parameters

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Format|String|No|The format in which to return the response. Valid values: -   JSON. This is the default value.
-   XML |
|Version|String|Yes|The version number of the API. The value is in the YYYY-MM-DD format. Valid value: 2019-01-01 |
|Signature|String|Yes|The signature string of the request.|
|SignatureMethod|String|Yes|The signature method. Set the value to HMAC-SHA1.|
|SignatureNonce|String|Yes|A unique, random number used to prevent replay attacks. You must use different numbers for different requests.|
|SignatureVersion|String|Yes|The version of the signature encryption algorithm. Set the value to 1.0.|
|AccessKeyId|String|Yes|The AccessKey ID provided to you by Alibaba Cloud.|
|Timestamp|String|Yes|The timestamp of the request. Specify the time in the ISO 8601 standard in the yyyy-MM-ddTHH:mm:ssZ format. The time must be in UTC. For example, 2013-01-10T12:00:00Z indicates 20:00:00 on January 10, 2013 \(UTC+8\). |

Sample requests

```
https://cloudmonitor.aliyuncs.com/?Action=CreateMonitorGroup
&Format=JSON
&Version=2019-01-01
&Signature=Pc5WB8gokVn0xfeu%2FZV%2BiNM1dg****
&SignatureMethod=HMAC-SHA1
&SignatureNonce=1521552885****
&SignatureVersion=1.0
&AccessKeyId=LTAI4GENiH2u8MVj7Khh****
&Timestamp=2020-06-01T12:00:00Z
```

## Common response parameters

Responses can be returned in the JSON or XML format. You can specify the response format in the request. The default response format is JSON. Every response returns a unique RequestId value regardless of whether the call is successful.

-   A `2xx` HTTP status code indicates a successful call.
-   A `4xx` or `5xx` HTTP status code indicates a failed call.

Sample responses

-   XML format

    ```
    <? xml version="1.0" encoding="utf-8"? > 
        <!--Root node of the response-->
        <Operation name+Response>
            <!--Return request data-->
            <RequestId>4C467B38-3910-447D-87BC-AC049166F216</RequestId>
            <!--Return result data-->
        </Operation name+Response>                        
    ```

-   JSON format

    ```
    {
        "RequestId":"4C467B38-3910-447D-87BC-AC049166F216"
        /*Return result data*/
    }
    ```


