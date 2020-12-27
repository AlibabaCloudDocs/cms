# 云监控ECS的Windows主机CPU监控数值异常

本文为您介绍云监控ECS的Windows主机CPU监控数值异常的原因及解决办法。

云监控中的ECS CPU监控数值如果出现为0或者负数（实际CPU使用率不是0），其他监控值都正常。这个问题主要出现在Windows的机器上，一般原因是Windows内部的性能计数器损坏了。

可以通过typeperf "\\Processor\(\_Total\)\\% Processor Time"查看计数器是否正常。如果提示“错误：没有有效计数器”，则说明计数器已损坏，可通过lodctr /r命令进行修复。

相关截图如下：

![查看计数器](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/7086958951/p5122.jpg)

