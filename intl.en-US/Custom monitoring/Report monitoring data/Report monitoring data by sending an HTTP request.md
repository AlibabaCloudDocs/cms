# Report monitoring data by sending an HTTP request

This topic describes how to report monitoring data by sending an HTTP request.

## Endpoints

-   Public endpoint: `https://metrichub-cms-cn-hangzhou.aliyuncs.com`.
-   The following table describes the internal endpoints in different regions.

    |Region|Region ID|Endpoint|
    |:-----|:--------|:-------|
    |China \(Hangzhou\)|cn-hangzhou|http://metrichub-cn-hangzhou.aliyun.com|
    |China \(Zhangjiakou\)|cn-zhangjiakou|http://metrichub-cn-zhangjiakou.aliyun.com|
    |China \(Shanghai\)|cn-shanghai|http://metrichub-cn-shanghai.aliyun.com|
    |China \(Beijing\)|cn-beijing|http://metrichub-cn-beijing.aliyun.com|
    |China \(Qingdao\)|cn-qingdao|http://metrichub-cn-qingdao.aliyun.com|
    |China \(Shenzhen\)|cn-shenzhen|http://metrichub-cn-shenzhen.aliyun.com|
    |China \(Hong Kong\)|cn-hongkong|http://metrichub-cn-hongkong.aliyun.com|
    |China \(Hohhot\)|cn-huhehaote|http://metrichub-cn-huhehaote.aliyun.com|
    |UAE \(Dubai\)|me-east-1|http://metrichub-me-east-1.aliyun.com|
    |US \(Silicon Valley\)|us-west-1|http://metrichub-us-west-1.aliyun.com|
    |US \(Virginia\)|us-east-1|http://metrichub-us-east-1.aliyun.com|
    |Japan \(Tokyo\)|ap-northeast-1|http://metrichub-ap-northeast-1.aliyun.com|
    |Germany \(Frankfurt\)|eu-central-1|http://metrichub-eu-central-1.aliyun.com|
    |Australia \(Sydney\)|ap-southeast-2|http://metrichub-ap-southeast-2.aliyun.com|
    |Singapore|ap-southeast-1|http://metrichub-ap-southeast-1.aliyun.com|
    |Malaysia \(Kuala Lumpur\)|ap-southeast-3|http://metrichub-ap-southeast-3.aliyun.com|
    |India \(Mumbai\)|ap-south-1|http://metrichub-ap-south-1.aliyuncs.com|


## Request syntax

An HTTP request for reporting monitoring data is in the following syntax:

```
POST /metric/custom/upload HTTP/1.1 
Authorization:<AuthorizationString>
Content-Length:<Content Length>
Content-MD5:<Content MD5>
Content-Type:application/json
Date:<GMT Date>
Host: metrichub-cms-cn-hangzhou.aliyuncs.com
x-cms-signature:hmac-sha1
x-cms-api-version:1.0
x-cms-ip:30.27.XX.XX
User-Agent:cms-java-sdk-v-1.0
[{"groupId":XXX,"metricName":"diskUtilization","dimensions":{"instanceId":"i-abcdefgh12****","disk":"/"},"time":"20190701T12345.888+0800","type":0,"period":60,"values":{"value":60}}]
```

## Request parameters

The following tables describe the headers and parameters in an HTTP request for reporting monitoring data.

-   Request headers

    |Header|Type|Description|
    |:-----|:---|:----------|
    |Authorization|String|The authorization string, in the format of `AccessKeyID:SignString`.For more information about how to obtain the AccessKey ID, see [Obtain an AccessKey pair](). |
    |Content-Length|Long|The length of the HTTP request body, as defined in RFC 2616. This header is only required when the request has a body.|
    |Content-MD5|String|The MD5 value of the HTTP request body. The MD5 value is a string consisting of uppercase letters and digits. This header is only required when the request has a body.|
    |Content-Type|String|The type of the content that is sent in the HTTP request. Set the value to `application/json`.|
    |Date|String|The standard timestamp header of the HTTP request. This timestamp header follows the time format defined in RFC 1123 and uses the GMT standard time. Example: `Mon, 3 Jan 2010 08:33:47 GMT`. |
    |Host|String|The full hostname of the HTTP request. This header does not include the protocol header such as https://. Example: `metrichub-cms-cn-hangzhou.aliyuncs.com`. |
    |x-cms-api-version|String|The version of the API. Set the value to 1.0.|
    |x-cms-signature|String|The signature algorithm. Cloud Monitor supports only the HMAC-SHA1 signature algorithm. For more information, see [Does CloudMonitor support the HMAC-SHA1 signature algorithm and how do I use it?](/intl.en-US/FAQ/Operation/Does CloudMonitor support the HMAC-SHA1 signature algorithm and how do I use it?.md)|
    |x-cms-ip|String|The IP address of the host that reports the monitoring data.|
    |User-Agent|String|The description of the client.|

-   Request parameters

    |Parameter|Type|Required|Description|
    |:--------|:---|:-------|:----------|
    |groupId|Long|Yes|The ID of the application group.|
    |metricName|String|Yes|The name of the metric. The metric name can contain letters, digits, underscores \(\_\), hyphens \(-\), periods \(.\), forward slashes \(/\), and backslashes \(\\\). The metric name can be up to 64 bytes in length. Excessive characters are truncated.|
    |dimensions|Object|Yes|The map of the monitored resources. The value is a collection of key-value pairs. A typical pair is instanceId:i-abcdefgh12\*\*\*\*.

The key and value can be 1 to 64 bytes in length. Excessive characters are truncated.

The key and value can contain letters, digits, periods \(.\), hyphens \(-\), underscores \(\_\), forward slashes \(/\), and backslashes \(\\\). |
    |time|String|Yes|The timestamp when the metric data is generated. The timestamp can be in one of the following formats:     -   yyyyMMdd'T'HHmmss.SSSZ

Example: 20171012T132456.888+0800.

    -   Long

Example: 1508136760000. |
    |type|Int|Yes|The type of the reported data. Valid values: 0 and 1. The value 0 indicates raw data and the value 1 indicates aggregate data.

We recommend that you report aggregate data in both the aggregation periods of 60s and 300s. Otherwise, you cannot query monitoring data in a time span that is more than seven days. |
    |period|String|No|The aggregation period. Unit: seconds.

If the type parameter is set to 1, the period parameter is required. Valid values:

    -   60
    -   300 |
    |values|Object|Yes|The collection of metric values. If the type parameter is set to 0, the keys in this parameter must be set to the specified value. Cloud Monitor aggregates raw data in each aggregation period to generate multiple statistical values, such as the maximum value, the count, and the total value. |


## Sample response

The following content shows the sample response to an HTTP request for reporting monitoring data:

```
{
  "code":"200",// The HTTP status code 200 indicates that the request was successful.
  "msg":""// The value is empty when monitoring data is reported.
}
```

