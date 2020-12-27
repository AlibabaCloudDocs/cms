# 禁用ECS的内网后不能使用云监控

本文为您介绍为何禁用ECS的内网后不能使用云监控。

ECS服务器使用云监控服务，是不能禁用内网的。

因为云监控的通讯地址open.cms.aliyun.com是解析在内网上的，通过内网来进行通讯获取数据，如果禁用了内网，云监控服务会出现无法正常使用，所以为了能够正常的使用云监控服务，必须要确保在服务器上能连通open.cms.aliyun.com的80端口。

![Telnet](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/4086958951/p127555.png)

