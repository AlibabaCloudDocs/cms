# 通过HTTP上报监控数据

本文为您介绍通过HTTP上报监控数据的配置方法。

## 服务地址

-   公网服务地址：`https://metrichub-cms-cn-hangzhou.aliyuncs.com`。
-   内网服务地址如下表所示。

    |地域|RegionId|服务地址|
    |:-|:-------|:---|
    |华东1（杭州）|cn-hangzhou|http://metrichub-cn-hangzhou.aliyun.com|
    |华北3（张家口）|cn-zhangjiakou|http://metrichub-cn-zhangjiakou.aliyun.com|
    |华东2（上海）|cn-shanghai|http://metrichub-cn-shanghai.aliyun.com|
    |华北2（北京）|cn-beijing|http://metrichub-cn-beijing.aliyun.com|
    |华北1（青岛）|cn-qingdao|http://metrichub-cn-qingdao.aliyun.com|
    |华南1（深圳）|cn-shenzhen|http://metrichub-cn-shenzhen.aliyun.com|
    |中国（香港）|cn-hongkong|http://metrichub-cn-hongkong.aliyun.com|
    |华北5 （呼和浩特）|cn-huhehaote|http://metrichub-cn-huhehaote.aliyun.com|
    |阿联酋（迪拜）|me-east-1|http://metrichub-me-east-1.aliyun.com|
    |美国（硅谷 ）|us-west-1|http://metrichub-us-west-1.aliyun.com|
    |美国（弗吉尼亚）|us-east-1|http://metrichub-us-east-1.aliyun.com|
    |日本（东京 ）|ap-northeast-1|http://metrichub-ap-northeast-1.aliyun.com|
    |德国（法兰克福）|eu-central-1|http://metrichub-eu-central-1.aliyun.com|
    |澳大利亚（悉尼）|ap-southeast-2|http://metrichub-ap-southeast-2.aliyun.com|
    |新加坡|ap-southeast-1|http://metrichub-ap-southeast-1.aliyun.com|
    |马来西亚（吉隆坡）|ap-southeast-3|http://metrichub-ap-southeast-3.aliyun.com|
    |印度（孟买）|ap-south-1|http://metrichub-ap-south-1.aliyuncs.com|


## 请求语法

通过HTTP方式上报监控数据的请求语法如下：

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

## 请求参数

通过HTTP方式上报监控数据的请求参数和请求头说明如下表所示。

-   请求头

    |Header|类型|描述|
    |:-----|:-|:-|
    |Authorization|String|内容：`AccessKeyId:SignString`。AccessKey ID的获取方法请参见[获取AccessKey]()。 |
    |Content-Length|Long|RFC 2616中定义的HTTP请求的Body长度。如果请求无Body部分，则无需提供该请求头。|
    |Content-MD5|String|请求Body经过MD5计算后的字符串，计算结果为大写字母和数字字符串。如果请求无Body部分，则无需提供该请求头。|
    |Content-Type|String|发送端发送的实体数据的数据类型。只支持`application/json`。|
    |Date|String|HTTP请求中的标准时间头（遵循RFC 1123格式，使用GMT标准时间）。 示例：`Mon, 3 Jan 2010 08:33:47 GMT`。 |
    |Host|String|HTTP请求的完整Host名称（不包括如https://这样的协议头）。 示例：`metrichub-cms-cn-hangzhou.aliyuncs.com` |
    |x-cms-api-version|String|API版本。当前版本1.0。|
    |x-cms-signature|String|签名算法。目前，云监控只支持数字签名算法HMAC-SHA1，请参见[签名算法：HMAC-SHA1](/intl.zh-CN/常见问题/产品使用问题/签名算法：HMAC-SHA1.md)。|
    |x-cms-ip|String|上报监控数据的服务器IP地址。|
    |User-Agent|String|客户端说明。|

-   请求参数

    |名称|类型|是否必选|描述|
    |:-|:-|:---|:-|
    |groupId|Long|是|应用分组ID。|
    |metricName|String|是|监控项名称。支持大小写字母、数字、下划线（\_）、短划线（-）、英文句点（.）、正斜线（/）和反斜线（\\），最大长度为64字节，超过64字节时截取前64字节。|
    |dimensions|Object|是|维度Map，用于查询指定资源的监控数据。 格式为：key-value键值对形式的集合，常用的key-value集合为：instanceId:i-abcdefgh12\*\*\*\*。

Key和Value的长度为1~64个字节，超过64个字节时截取前64字节。

Key和Value的取值可包含大小写字母、数字、英文句点（.）、短划线（-）、下划线（\_）、正斜线（/）和反斜线（\\）。 |
    |time|String|是|指标生成时间。支持的格式如下：    -   yyyyMMdd’T’HHmmss.SSSZ

例如：20171012T132456.888+0800

    -   long

例如：1508136760000 |
    |type|Int|是|上报数值的类型。0为原始值，1为聚合数据。

当上报聚合数据时，建议上报60秒和300秒的数据，否则无法正常查询跨度大于7天的监控数据。 |
    |period|String|否|聚合周期。单位：秒。

如果type为1，则需要上传该参数，取值：

    -   60
    -   300 |
    |values|Object|是|指标值集合。 如果type为0，则Key只能与Value相同，上报原始值，云监控会按周期将原始值聚合为多个值。例如：最大、计数、求和等。 |


## 返回示例

通过HTTP方式上报监控数据的代码返回示例如下：

```
{
  "code":"200",//200表示成功。
  "msg":""//正常上报时返回msg为空。
}
```

