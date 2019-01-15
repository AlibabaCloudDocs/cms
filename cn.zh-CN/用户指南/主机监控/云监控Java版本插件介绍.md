# 云监控Java版本插件介绍 {#concept_rfs_thv_vdb .concept}

云监控主机监控服务是通过在服务器上安装插件，为用户提供服务器的系统监控服务的。

## 安装位置 {#section_lct_qk2_xdb .section}

-   Linux：/usr/local/cloudmonitor
-   Windows： C:\\Program Files\\Alibaba\\cloudmonitor

## 进程信息 {#section_ow1_rq2_xdb .section}

插件安装后，会在您的服务器上运行以下两个进程：

-   /usr/local/cloudmonitor/jre/bin/java
-   /usr/local/cloudmonitor/wrapper/bin/wrapper

## 端口说明 {#section_z3f_vq2_xdb .section}

-   通过TCP协议监听、访问本地主机的32000端口， 用于守护进程。
-   通过TCP协议访问远程服务器的3128、8080、443端口， 用于心跳联网与监控数据上报，非阿里云主机使用443端口，阿里云主机使用3128或8080端口。
-   通过HTTP协议访问远程服务器的80端口，用于云监控插件升级。

## 插件日志 {#section_gkl_wq2_xdb .section}

-   监控数据日志位于/usr/local/cloudmonitor/logs 。
-   启动、关闭、守护进程等日志位于 /usr/local/cloudmonitor/wrapper/logs 。
-   可以通过修改/usr/local/cloudmonitor/config/log4j.properties配置来调整日志级别。

## 资源占用情况 {#section_mmw_252_xdb .section}

-   /usr/local/cloudmonitor/wrapper/bin/wrapper进程占用1M左右内存，基本不消耗CPU。
-   /usr/local/cloudmonitor/jre/bin/java进程占用70M左右内存和1~2%的单核CPU。
-   安装包大小70M，安装完成后约占用200M磁盘空间。
-   日志最多占用40M空间，超过40M会进行清除。
-   每15秒发送一次监控数据，约占用内网网络带宽10KB。
-   每3分钟发送一次心跳数据，约占用内网网络带宽2KB左右。

## 外部依赖 {#section_x3b_lw2_xdb .section}

-   云监控Java版本插件，使用Java语言编写，内置JRE 1.8。
-   Java service wrapper 用于守护进程、开机启动、Windows服务注册等。
-   `ss -s`命令用于采集TCP连接数，如果当前系统没有此命令，需要您自己安装iproute。

## 安装说明 {#section_yhh_xw2_xdb .section}

请参见[云监控Java版本插件安装](intl.zh-CN/用户指南/主机监控/云监控Java版本插件安装.md#)。

## 非阿里云主机安装方法 {#section_a12_cx2_xdb .section}

1.  登录[云监控控制台](https://cms-intl.console.aliyun.com)。
2.  单击左侧导航栏中的**主机监控**，进入主机监控页面。
3.  单击页面上方的**非阿里云主机安装**按钮，进入监控安装指引页面，选择监控类型、操作系统后，可查看与其对应的安装方法。

