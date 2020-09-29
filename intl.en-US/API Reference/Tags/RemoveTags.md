# RemoveTags

Deletes one or more tags.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=RemoveTags&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|RemoveTags|The operation that you want to perform. Set the value to RemoveTags. |
|GroupIds.N|RepeatList|Yes|12345|The ID of the application group. |
|Tag.N.Key|String|Yes|Key1|The key of the tag.

**Note:** The `Tag.N.Key` and `Tag.N.Value` parameters must be used in pairs. |
|Tag.N.Value|String|Yes|Value1|The value of the tag.

**Note:** The `Tag.N.Key` and `Tag.N.Value` parameters must be used in pairs. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|195390D2-69D0-4D9E-81AA-A7F5BC1B91EB|The ID of the request. |
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |
|Tag|List|tag1|The deleted tags. |
|Message|String|Illegal parameters.|The returned message. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=RemoveTags
&GroupIds.1=12345
&Tag.1.Key=Key1
&Tag.1.Value=Value1
&<Common request parameters>
```

Sample success responses

`XML` format

```
<RemoveTagsResponse>
          <RequestId>E15C718E-067E-49D0-86F7-BC7242230091</RequestId>
          <Code>200</Code>
          <Success>true</Success>
</RemoveTagsResponse>
```

`JSON` format

```
{
    "RequestId": "E15C718E-067E-49D0-86F7-BC7242230091",
    "Code": 200,
    "Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

