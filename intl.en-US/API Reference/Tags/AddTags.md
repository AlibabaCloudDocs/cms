# AddTags

Creates one or more tags for the specified resources.

**Note:** You can create tags only for application groups.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=AddTags&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|AddTags|The operation that you want to perform. Set the value to AddTags. |
|GroupIds.N|RepeatList|Yes|12345|The ID of the application group. |
|Tag.N.Key|String|Yes|key1|The key of the tag.

Valid values of N: 1 to 3. The key can be 1 to 64 characters in length.

**Note:** The value of N cannot be empty or start with `aliyun` or `acs:`. The `Tag.N.Key` and `Tag.N.Value` parameters must be used in pairs. |
|Tag.N.Value|String|Yes|value1|The value of the tag. Valid values of N: 1 to 3. The value can be 1 to 64 characters in length.

**Note:** The value of N cannot be empty or start with `aliyun` or `acs:`. The `Tag.N.Key` and `Tag.N.Value` parameters must be used in pairs. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|B04B8CF3-4489-432D-83BA-6F128E4F2295|The ID of the request. |
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |
|Message|String|The Request is not authorization.|The returned message. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=AddTags
&GroupIds.1=12345
&Tag.1.Key=key1
&Tag.1.Value=value1
&<Common request parameters>
```

Sample success responses

`XML` format

```
<AddTagsResponse>
          <Code>200</Code>
          <RequestId>B04B8CF3-4489-432D-83BA-6F128E4F2295</RequestId>
          <Success>true</Success>
</AddTagsResponse>
```

`JSON` format

```
{
    "Code":"200",
    "RequestId":"B04B8CF3-4489-432D-83BA-6F128E4F2295",
    "Success":true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

