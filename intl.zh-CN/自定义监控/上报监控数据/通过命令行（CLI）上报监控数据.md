# 通过命令行（CLI）上报监控数据

本文为您介绍通过命令行上报监控数据的配置方法。

## 授权云监控管理权限

云监控支持使用阿里云账号和RAM用户上报监控数据。当RAM用户使用AccessKey上报监控数据时，需要授权云监控的管理权限。操作方法如下：

1.  使用阿里云账号登录[RAM控制台](https://ram.console.aliyun.com/)。
2.  创建RAM用户。

    操作方法请参见[创建RAM用户](/intl.zh-CN/用户管理/创建RAM用户.md)。

3.  为RAM用户创建访问密钥。

    操作方法请参见[为RAM用户创建访问密钥](/intl.zh-CN/安全设置/访问密钥/为RAM用户创建访问密钥.md)。

4.  为RAM用户授权（AliyunCloudMonitorFullAccess）。

    操作方法请参见[为RAM用户授权](/intl.zh-CN/用户管理/为RAM用户授权.md)。


## 安装和配置阿里云命令行（CLI）工具

安装阿里云命令行（CLI）工具，操作方法请参见[在Windows上安装阿里云CLI](https://www.alibabacloud.com/help/doc-detail/121510.htm)或[在Linux上安装阿里云CLI](https://www.alibabacloud.com/help/doc-detail/121541.htm)。

## 上报监控数据

使用PutCustomMetric接口上报自定义监控数据，请参见[PutCustomMetric](/intl.zh-CN/API参考/自定义监控/PutCustomMetric.md)。

示例如下：

```
aliyun cms PutCustomMetric  --MetricList.1.MetricName cpu_total --MetricList.1.Dimensions '{"sampleName1":"value1","sampleName2":"value2"}' --MetricList.1.Time 1555390981421 --MetricList.1.Type 0 --MetricList.1.Period 60 --MetricList.1.Values '{"value":10.5}' --MetricList.1.GroupId "0"
```

上报监控数据成功后，返回状态码200。

```
{
  "Message": "success",
  "RequestId": "F69F5623-DDD6-42AE-AE59-87A2B841620B",
  "Code": "200"
}
```

## 状态码说明

当通过命令行上报监控数据时，返回的状态码如下表所示。

|状态码|描述|
|:--|:-|
|200|正常|
|206|-   返回信息为`“reach max time series num”`，表示您的可用时间序列配额已用完，需要购买更多配额或删除不再使用的时间序列。
-   返回信息为`“not allowed original value, please upgrade service”`，表示您使用的是免费版云监控，无法使用上报原始数据功能。
-   返回信息为`“type is invalid”` ，表示Type参数错误，请检查是否传入了0或1以外的数值。 |
|400|表示客户端请求中的语法错误。|
|403|表示校验失败、限速或没有授权。|
|500|表示服务器内部错误。|

