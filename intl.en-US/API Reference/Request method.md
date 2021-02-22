# Request method

To send a Cloud Monitor API request, you must send an HTTP GET request to the Cloud Monitor endpoint. You must add the request parameters that correspond to the API operation being called. After you call the API operation, the system returns a response. The request and response are encoded in UTF-8.

## Request syntax

Cloud Monitor API operations use the RPC protocol. You can call Cloud Monitor API operations by sending HTTP GET requests.

The following request syntax is used:

`http://endpoint/?Action=xx&parameters`

where:

-   `Endpoint`: the endpoint of the Cloud Monitor API is `metrics.aliyuncs.com`. For more information about the endpoints of various regions, see [Cloud Monitor endpoints](#section_xf3_lbv_zdb).
-   `Action`: the operation that you want to perform. For example, to query the monitoring data of an instance, you set the Action parameter to DescribeMetricList.
-   `Version`: the version number of the API. The version number of the Cloud Monitor API is 2019-01-01.
-   `Parameters`: the request parameters for the operation. Separate multiple parameters with ampersands \(&\). Request parameters include both common parameters and operation-specific parameters. Common parameters include information such as the API version number and authentication information.

The following example demonstrates how to call the DescribeMetricList operation in Cloud Monitor:

```
http://metrics.cn-hangzhou.aliyuncs.com/?Action=DescribeMetricList
&EndTime=2020-06-01 00:00:00
&StartTime=2020-06-30 00:00:00
&Period=60
&Dimensions={"instanceId": "i-uf6hm9lnlzsarrc7****"}
&Timestamp=1490152860000
&Namespace=acs_ecs_dashboard
&Metric=cpu_idle
```

## Cloud Monitor endpoints

|Region|Endpoint|
|:-----|:-------|
|China \(Qingdao\)|metrics.cn-qingdao.aliyuncs.com|
|China \(Beijing\)|metrics.cn-beijing.aliyuncs.com|
|China \(Zhangjiakou-Beijing Winter Olympics\)|metrics.cn-zhangjiakou.aliyuncs.com|
|China \(Hohhot\)|metrics.cn-huhehaote.aliyuncs.com|
|China \(Hangzhou\)|metrics.cn-hangzhou.aliyuncs.com|
|China \(Shanghai\)|metrics.cn-shanghai.aliyuncs.com|
|China \(Shenzhen\)|metrics.cn-shenzhen.aliyuncs.com|
|China \(Hong Kong\)|metrics.cn-hongkong.aliyuncs.com|
|Singapore \(Singapore\)|metrics.ap-southeast-1.aliyuncs.com|
|Australia \(Sydney\)|metrics.ap-southeast-2.aliyuncs.com|
|Malaysia \(Kuala Lumpur\)|metrics.ap-southeast-3.aliyuncs.com|
|Indonesia \(Jakarta\)|metrics.ap-southeast-5.aliyuncs.com|
|India \(Mumbai\)|metrics.ap-south-1.aliyuncs.com|
|Japan \(Tokyo\)|metrics.ap-northeast-1.aliyuncs.com|
|US \(Silicon Valley\)|metrics.us-west-1.aliyuncs.com|
|US \(Virginia\)|metrics.us-east-1.aliyuncs.com|
|Germany \(Frankfurt\)|metrics.eu-central-1.aliyuncs.com|
|UK \(London\)|metrics.eu-west-1.aliyuncs.com|
|UAE \(Dubai\)|metrics.me-east-1.aliyuncs.com|

## API authorization

To ensure the security of your account, we recommend that you call Cloud Monitor API operations as a Resource Access Management \(RAM\) user. If you call Cloud Monitor API operations as a RAM user , you must create permission policies for or grant permission policies to the RAM user .

## Signature method

To ensure secure calls to the API, Alibaba Cloud authenticates each API request by using the signature. When you manually make an API request, you must use the AccessKey secret to calculate the hash-based message authentication code \(HMAC\) value based on the encoded and sorted request string in accordance with the definition in [RFC 2104](https://www.ietf.org/rfc/rfc2104.txt?spm=a2c4g.11186623.2.6.tstgdp&file=rfc2104.txt). The HMAC value is the signature. For more information, see [Does CloudMonitor support the HMAC-SHA1 signature algorithm and how do I use it?](/intl.en-US/FAQ/Operations/Does CloudMonitor support the HMAC-SHA1 signature algorithm and how do I use it?.md).

You must add the signature to the Cloud Monitor API request in the following format:

`https://endpoint/?SignatureVersion=1.0&SignatureMethod=HMAC-SHA1&Signature=CT9X0VtwR86fNWSnsc6v8YGOjuE%3D&SignatureNonce=3ee8c1b8-83d3-44af-a94f-4e0ad82f****`

Take DescribeMetricList as an example. If the AccessKey ID is `testid` and the AccessKey secret is `testsecret`, the following URL is the original request URL:

```
http://metrics.aliyuncs.com/?Action=DescribeMetricList&period=60&StartTime=2016-03-22T11:30:27Z&Dimensions={instanceId:'i-abcdefgh12****'}&Timestamp=2017-03-23T06:59:55Z&Namespace=acs_ecs_dashboard&SignatureVersion=1.0&Format=JSON&SignatureNonce=aeb03861-611f-43c6-9c07-b752fad3****&Version=2015-10-20&AccessKeyId=TestId&MetricName=cpu_idle&SignatureMethod=HMAC-SHA1
```

The following string is the string to sign:

```
GET&%2F&AccessKeyId%3DTestId&Action%3DDescribeMetricList&Dimensions%3D%257B%2522instanceId%2522%253A%2522i-abcdefgh123456%2522%257D&Format%3DJSON&Metric%3Dcpu_idle&Period%3D60&Namespace%3Dacs_ecs_dashboard&SignatureMethod%3DHMAC-SHA1&SignatureNonce%3Daeb03861-611f-43c6-9c07-b752fad3****&SignatureVersion%3D1.0&StartTime%3D2016-03-22T11%253A30%253A27Z&Timestamp%3D2017-03-23T06%253A59%253A55Z&Version%3D2015-10-20
```

The AccessKey secret is `testsecret`, so the key for the HMAC calculation is `testsecret&`. The following string is the calculated signature string:

```
TLj49H/wqBWGJ7RK0r84SN5I****
```

Add the signature string as the Signature parameter to the request URL. The following URL is the signed request URL:

```
http://metrics.cn-hangzhou.aliyuncs.com/?Action=DescribeMetricList&StartTime=2016-03-22T11%3A30%3A27Z&Period=60&Dimensions=%7B%22instanceId%22%3A%22i-abcdefgh123456%22%7D&Timestamp=2017-03-23T06%3A59%3A55Z&Namespace=acs_ecs_dashboard&SignatureVersion=1.0&Format=JSON&SignatureNonce=aeb03861-611f-43c6-9c07-b752fad3dc06&Version=2015-10-20&AccessKeyId=TestId&Metric=cpu_idle&SignatureMethod=HMAC-SHA1&Signature=TLj49H%2FwqBWGJ7RK0r84SN5****%3D
```

