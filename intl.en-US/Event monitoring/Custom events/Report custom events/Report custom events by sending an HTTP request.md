# Report custom events by sending an HTTP request

This topic describes how to report custom events by sending an HTTP request.

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

An HTTP request for reporting custom events is in the following syntax:

```
POST /event/custom/upload HTTP/1.1 
Authorization:<AuthorizationString>
Content-Length:<Content Length>
Content-MD5:<Content MD5>
Content-Type:application/json
Date:<GMT Date>
Host:metrichub-cms-cn-hangzhou.aliyuncs.com
x-cms-signature:hmac-sha1
x-cms-api-version:1.0
x-cms-ip:30.27.XX.XX
User-Agent:cms-java-sdk-v-1.0
[{"content":"EventContent","groupId":GroupId,"name":"EventName","time":"20171023T144439.948+0800"}]
```

## Request headers and parameters

The following tables describe the headers and parameters in an HTTP request for reporting custom events.

-   Request headers

    |Header|Type|Description|
    |:-----|:---|:----------|
    |Authorization|String|The authorization string, in the format of `AccessKeyID:SignString`.For more information about how to obtain the AccessKey ID, see [Obtain an AccessKey pair](). |
    |Content-Length|Long|The length of the HTTP request body, as defined in RFC 2616. This header is required only when the request has a body.|
    |Content-MD5|String|The MD5 value of the HTTP request body. The MD5 value is a string consisting of uppercase letters and digits. This header is required only when the request has a body.|
    |Content-Type|String|The type of the content that is sent in the HTTP request. Set the value to `application/json`.|
    |Date|String|The standard timestamp header of the HTTP request. This timestamp header follows the time format defined in RFC 1123 and uses the GMT standard time. Example: `Mon, 3 Jan 2010 08:33:47 GMT`. |
    |Host|String|The full hostname of the HTTP request. This header does not include the protocol header such as https://. Example: `metrichub-cms-cn-hangzhou.aliyuncs.com`. |
    |x-cms-api-version|String|The version of the API. Set the value to 1.0.|
    |x-cms-signature|String|The signature algorithm. Cloud Monitor supports only the HMAC-SHA1 signature algorithm. For more information, see [Does CloudMonitor support the HMAC-SHA1 signature algorithm and how do I use it?](/intl.en-US/FAQ/Operation/Does CloudMonitor support the HMAC-SHA1 signature algorithm and how do I use it?.md)|
    |x-cms-ip|String|The IP address of the host that reports the custom events.|
    |User-Agent|String|The description of the client.|

-   Request parameters

    |Parameter|Type|Required|Description|
    |:--------|:---|:-------|:----------|
    |content|String|Yes|The details of the custom event.|
    |name|String|Yes|The name of the custom event.|
    |groupId|Long|No|The ID of the application group to which the custom event belongs.|
    |time|String|No|The time when the custom event occurred.|


## Sample response

The following content shows the sample response to an HTTP request for reporting custom events:

```
{
  "code":"200",// The HTTP status code 200 indicates that the request was successful.
  "msg":""// The value is empty when the events are reported.
}
```

