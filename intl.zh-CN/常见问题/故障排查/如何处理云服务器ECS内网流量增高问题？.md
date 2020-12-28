# 如何处理云服务器ECS内网流量增高问题？

本文为您介绍如何处理云服务器ECS内网流量增高问题。

## 问题描述

在云监控控制台的主机监控中，看到云服务器ECS的内网流量增高，如下图所示。

![内网流量](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/8583319061/p4956.jpg)

## 问题分析

云服务器ECS通过外网网卡对外提供服务，内网的使用率通常比较低。当其他ECS服务器向某个ECS服务器拷贝数据时，会导致当前服务器内网流量增高。

**说明：** 负载均衡SLB除外，因为负载均衡SLB通过内网与云服务器ECS通信。

如果非数据拷贝问题，则可能是云服务器ECS中毒，对外大量发包导致内网流量增高。此时，处理方法请参见[处理方法](#section_okc_l6y_6la)。

## 处理方法

云服务器ECS部署在Linux和Windows上的处理方法如下：

-   Linux

    **说明：** NetHogs是一个开源的命令行工具（类似于Linux的top命令），用来按进程或程序实时统计网络带宽使用率。

    1.  下载NetHogs。
    2.  执行以下命令，安装NetHogs。

        yum install nethogs

    3.  执行以下命令，查看占用内网带宽的进程。

        nethogseth0

        ![nethogs](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/3086958951/p4957.jpg)

-   Windows

    **说明：** Windows Server 2008及以上的操作系统，您可以通过资源监视器查看占用内网带宽的进程。

    1.  在云服务器ECS的任务栏上，单击鼠标右键，选择**任务管理器**。
    2.  在任务管理器的**进程**页签，查看占用内网带宽的进程。

