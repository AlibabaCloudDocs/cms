# Why is the CPU utilization displayed as 0% in the Cloud Monitor console?

This topic describes why the CPU utilization is displayed as 0% in the Cloud Monitor console.

This issue is caused by low CPU utilization. The CPU utilization is around 0.5%, as shown in the following figure.

![](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/6339997951/p4963.jpg)

An Elastic Compute Service \(ECS\) instance reports the CPU utilization to Cloud Monitor once a minute. Cloud Monitor displays the average CPU utilization in the last five minutes in the console. If the average CPU utilization in the last five minutes is less than 0.5%, Cloud Monitor displays the CPU utilization as 0%.

![](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/6339997951/p4964.jpg)

