# 调用API

云监控接口调用是向云监控API的服务端地址发送HTTP GET请求，并按照接口说明在请求中加入相应请求参数，调用后系统会返回处理结果。请求及返回结果都使用UTF-8字符集进行编码。

## 请求结构

云监控的API是RPC风格，您可以通过发送HTTP请求调用云监控API。

其请求结构如下：

`http://endpoint/?Action=xx&parameters`

其中：

-   `Endpoint`是调用的云服务的接入点，云监控的接入点是`metrics.aliyuncs.com`。各地域的服务地址，参见[云监控接入地址](#section_xf3_lbv_zdb)。
-   `Action`是要执行的操作，如使用DescribeMetricList接口查询某一实例的监控数据。
-   `Version`要使用的API版本，云监控的API版本是2019-01-01。
-   `Parameters`是请求参数，每个参数之间用&分隔。请求参数由公共请求参数和API自定义参数组成。公共参数中包含API版本号、身份验证等信息。

下面是一个调用DescribeMetricList接口查询某一实例的监控数据的示例。

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

## 云监控接入地址

|地域名称|服务地址|
|:---|:---|
|华北 1（青岛）|metrics.cn-qingdao.aliyuncs.com|
|华北 2（北京）|metrics.cn-beijing.aliyuncs.com|
|华北 3（张家口）|metrics.cn-zhangjiakou.aliyuncs.com|
|华北 5（呼和浩特）|metrics.cn-huhehaote.aliyuncs.com|
|华东 1（杭州）|metrics.cn-hangzhou.aliyuncs.com|
|华东 2（上海）|metrics.cn-shanghai.aliyuncs.com|
|华南 1（深圳）|metrics.cn-shenzhen.aliyuncs.com|
|中国香港（香港）|metrics.cn-hongkong.aliyuncs.com|
|亚太东南 1（新加坡）|metrics.ap-southeast-1.aliyuncs.com|
|亚太东南 2（悉尼）|metrics.ap-southeast-2.aliyuncs.com|
|亚太东南 3（吉隆坡）|metrics.ap-southeast-3.aliyuncs.com|
|亚太东南 5（雅加达）|metrics.ap-southeast-5.aliyuncs.com|
|亚太南部 1（孟买）|metrics.ap-south-1.aliyuncs.com|
|亚太东北 1（东京）|metrics.ap-northeast-1.aliyuncs.com|
|美国西部 1（硅谷）|metrics.us-west-1.aliyuncs.com|
|美国东部 1（弗吉尼亚）|metrics.us-east-1.aliyuncs.com|
|欧洲中部 1（法兰克福）|metrics.eu-central-1.aliyuncs.com|
|英国（伦敦）|metrics.eu-west-1.aliyuncs.com|
|中东东部 1（迪拜）|metrics.me-east-1.aliyuncs.com|

## API授权

为了确保您的账号安全，建议您使用RAM用户的身份凭证调用API。如果您使用RAM用户调用云监控API，则您需要为该RAM用户创建或授予相应的权限策略。

## API签名

为保证API的安全调用，在调用API时阿里云会对每个API请求通过签名（Signature）进行身份验证。当您手动发起API请求时，需要按照[RFC 2104](https://www.ietf.org/rfc/rfc2104.txt?spm=a2c4g.11186623.2.6.tstgdp&file=rfc2104.txt)的定义，使用AccessSecret对编码、排序后的整个请求串计算HMAC值作为签名。更多详细信息，请参见[签名算法：HMAC-SHA1](/cn.zh-CN/常见问题/产品使用/签名算法：HMAC-SHA1.md)。

RPC API要按如下格式在API请求的中增加签名（Signature）：

`https://endpoint/?SignatureVersion=1.0&SignatureMethod=HMAC-SHA1&Signature=CT9X0VtwR86fNWSnsc6v8YGOjuE%3D&SignatureNonce=3ee8c1b8-83d3-44af-a94f-4e0ad82f****`

以DescribeMetricList为例，如果使用的AccessKey ID是`testid`，AccessKey Secret是 `testsecret`，则签名前的请求URL为：

```
http://metrics.aliyuncs.com/?Action=DescribeMetricList&period=60&StartTime=2016-03-22T11:30:27Z&Dimensions={instanceId:'i-abcdefgh12****'}&Timestamp=2017-03-23T06:59:55Z&Namespace=acs_ecs_dashboard&SignatureVersion=1.0&Format=JSON&SignatureNonce=aeb03861-611f-43c6-9c07-b752fad3****&Version=2015-10-20&AccessKeyId=TestId&MetricName=cpu_idle&SignatureMethod=HMAC-SHA1
```

计算得到的待签名字符串StringToSign为：

```
GET&%2F&AccessKeyId%3DTestId&Action%3DDescribeMetricList&Dimensions%3D%257B%2522instanceId%2522%253A%2522i-abcdefgh123456%2522%257D&Format%3DJSON&Metric%3Dcpu_idle&Period%3D60&Namespace%3Dacs_ecs_dashboard&SignatureMethod%3DHMAC-SHA1&SignatureNonce%3Daeb03861-611f-43c6-9c07-b752fad3****&SignatureVersion%3D1.0&StartTime%3D2016-03-22T11%253A30%253A27Z&Timestamp%3D2017-03-23T06%253A59%253A55Z&Version%3D2015-10-20
```

因为AccessKey Secret是`testsecret`，所以用于计算HMAC的Key为`testsecret&`，计算得到的签名值是：

```
TLj49H/wqBWGJ7RK0r84SN5I****
```

将签名作为Signature参数加入到URL请求中，得到最后的URL为：

```
http://metrics.cn-hangzhou.aliyuncs.com/?Action=DescribeMetricList&StartTime=2016-03-22T11%3A30%3A27Z&Period=60&Dimensions=%7B%22instanceId%22%3A%22i-abcdefgh123456%22%7D&Timestamp=2017-03-23T06%3A59%3A55Z&Namespace=acs_ecs_dashboard&SignatureVersion=1.0&Format=JSON&SignatureNonce=aeb03861-611f-43c6-9c07-b752fad3dc06&Version=2015-10-20&AccessKeyId=TestId&Metric=cpu_idle&SignatureMethod=HMAC-SHA1&Signature=TLj49H%2FwqBWGJ7RK0r84SN5****%3D
```

