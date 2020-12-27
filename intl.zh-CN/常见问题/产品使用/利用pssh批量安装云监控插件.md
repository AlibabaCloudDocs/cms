# 利用pssh批量安装云监控插件

本文为您介绍如何利用pssh批量安装云监控插件。

## pssh介绍

pssh 是一个python写的批量执行工具，非常适合30台服务器以内的一些重复性的操作。例如安装一个软件，kill 一个进程，下载文件等。

## 单机安装云监控插件

`**bash**-c "$(curl http://cloudmonitor-agent.oss-cn-hangzhou.aliyuncs.com/release/install.sh)"`

## 批量安装云监控插件

-   **安装pssh**
    1.  安装 python 2.4 以上。
    2.  安装 pssh 。

        ```
         wget https://pypi.python.org/packages/source/p/pssh/pssh-2.3.1.tar.gz
         tar zxf pssh-2.3.1.tar.gz
         cd pssh-2.3.1
         python setup.py install 
        							
        ```

-   **配置IP列表，准备安装云监控插件的主机**
    1.  配置ip.txt文件。
    2.  格式为user@ip:port每行一个，port不填默认为22。
    3.  执行命令的用户需要有sudo权限。
    4.  批量安装的机器，密码要相同，也可以配置无密码互信。
-   **批量执行**

    `pssh -h ip.txt -A -i bash -c "$(curl http://cloudmonitor-agent.oss-cn-hangzhou.aliyuncs.com/release/install.sh)"`

    -h host列表文件

    -A 手工输入密码，无密码互信不需要这个参数

    -i 执行的命令

-   **查看云监控插件是否安装成功**

    `pssh -h ip.txt -A -i"/usr/local/cloudmonitor/wrapper/bin/cloudmonitor.sh status"`


