# 通过Java SDK上报事件监控数据（推荐）

本文为您介绍通过Java SDK上报自定义事件监控数据的配置方法。

## 安装Java SDK

通过Maven安装Java SDK，需要添加的依赖如下：

```
<dependency>
            <groupId>com.aliyun.openservices</groupId>
            <artifactId>aliyun-cms</artifactId>
            <version>0.2.4</version>
</dependency>
```

## 代码示例

通过Java SDK方式上报事件监控数据的代码示例如下：

```
public void uploadEvent() throws CMSException, InterruptedException {
        //初始化客户端
        CMSClient cmsClient = new CMSClient(endpoint, accKey, secret);
       //构建2个事件上报
         CustomEventUploadRequest request = CustomEventUploadRequest.builder()
                    .append(CustomEvent.builder()
                            .setContent("abc,123")
                            .setGroupId(101l)
                            .setName("Event001").build())
                    .append(CustomEvent.builder()
                            .setContent("abc,123")
                            .setGroupId(101l)
                            .setName("Event002").build())
                    .build();
            CustomEventUploadResponse response = cmsClient.putCustomEvent(request);
            List<CustomEvent> eventList = new ArrayList<CustomEvent>();
            eventList.add(CustomEvent.builder()
                    .setContent("abcd,1234")
                    .setGroupId(101l)
                    .setName("Event001").build());
            eventList.add(CustomEvent.builder()
                    .setContent("abcd,1234")
                    .setGroupId(101l)
                    .setName("Event002").build());
            request = CustomEventUploadRequest.builder()
                    .setEventList(eventList).build();
            response = cmsClient.putCustomEvent(request);
    }
```

**说明：** endpoint是云服务的接入地址，云监控的接入地址为`metrics.aliyuncs.com`。云监控各地域的接入地址，请参见[服务地址](/cn.zh-CN/自定义监控/上报监控数据/通过HTTP上报监控数据.md)。

## 返回示例

通过Java SDK方式上报事件监控数据的代码返回示例如下：

```
{
    "Message": "success",
    "RequestId": "E25EE651-9C97-4EFD-AF22-A753B674E8D4",
    "Code": "200"
}
```

HTTP状态码返回200表示成功。

