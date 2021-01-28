# 非阿里云主机如何通过Nginx代理服务器上报监控数据？

本文为您介绍非阿里云主机通过Nginx代理服务器上报监控数据至云监控的操作方法。

## 步骤一：部署Nginx代理服务器

1.  下载Nginx最新安装包，例如：**nginx-1.19.6**。

    1.  登录[Nginx](https://nginx.org/en/download.html)下载中心。

    2.  单击**nginx-1.19.6**，下载Nginx安装包nginx-1.19.6.tar.gz。

2.  安装Nginx。

    **说明：** 由于云监控部署在Linux服务器上，因此建议您的代理服务器选用Linux服务器。

    1.  上传Nginx安装包nginx-1.19.6.tar.gz至代理服务器的指定目录，例如：/usr/local。

    2.  以root用户登录代理服务器。

    3.  执行以下命令，解压Nginx安装包nginx-1.19.6.tar.gz至目录nginx-1.19.6。

        cd /usr/local

        tar zxvfnginx-1.19.6.tar.gz

    4.  执行以下命令，初始化Nginx。

        cd nginx-1.19.6

        ./configure

    5.  执行以下命令，安装Nginx。

        make install

    6.  执行以下命令，启动Nginx。

        ./nginx

    7.  查看Nginx安装结果。

        在浏览器的地址栏输入代理服务器的IP地址:8080，显示如下，说明安装成功。

        ![Nginx](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/2061458061/p203666.png)

3.  配置Nginx。

    1.  执行以下命令，打开文件nginx.conf。

        cd conf

        vi nginx.conf

    2.  配置文件nginx.conf。

        在文件nginx.conf的末尾补充正向代理或反向代理的如下信息。正向代理和反向代理只能配置一个，否则配置无效。

        -   正向代理

            如果把局域网外的Internet想象成一个巨大的资源库，则局域网中的客户端要访问Internet，则需要通过代理服务器来访问，这种代理服务就称为正向代理。

            ```
            server {  
                    resolver 192.168.XX.XX;  #设置代理服务器的IP地址。  
                    listen 80;  
                    location / {  
                        proxy_pass http://$http_host$request_uri;  #设定代理服务器的协议和地址，均使用默认值。 
                    } 
            }
            ```

            **说明：** Nginx的正向代理不支持HTTPS协议。

        -   反向代理

            如果局域网向Internet提供资源服务，让Internet上的其他客户端来访问局域网内的资源，使他们必须通过一个代理服务器进行访问，这种服务就称为反向代理。

            ```
            server {
                    server_name 192.168.XX.XX; #设置代理服务器的IP地址。
                    listen 80;
                    location / {
                            proxy_pass https://www.aliyun.com; #设置代理服务器访问的URL地址。
                    }
            }
            ```

    3.  按Esc键，输入:wq，再按Enter键，保存并退出文件nginx.conf。

    4.  执行以下命令，重启Nginx代理服务器。

        nginx -s reload

    5.  测试Nginx安装结果

        -   正向代理

            执行以下命令，能访问任意网址，表示安装成功。

            curl -x192.168.XX.XX（代理服务器的IP地址）http://www.aliyun.com（任意网址）

        -   反向代理

            执行以下命令，无论输入任何网址，均只能访问文件nginx.conf中指定的网址，表示安装成功。

            curl -x192.168.XX.XX（代理服务器的IP地址）https://www.baidu.com（任意网址）


## 步骤二：安装和配置云监控插件

1.  在非阿里云主机上安装云监控插件。

    具体操作，请参见[安装和卸载插件](/cn.zh-CN/主机监控/云监控插件/安装和卸载插件.md)。

2.  在云监控插件中配置Nginx代理服务器。

    1.  以root用户登录云监控插件所在的非阿里云主机。

    2.  执行以下命令，打开文件agent.properties。

        cd /usr/local/cloudmonitor/conf

        vi agent.properties

    3.  在云监控插件中配置Nginx代理服务器的相关信息。

        配置方法如下：

        ```
        http.proxy.auto=false
        #手动配置代理
        http.proxy.host=192.168.XX.XX  #Nginx代理服务器的IP地址。
        http.proxy.port=8080  #Nginx代理服务器的端口。
        #http.proxy.user=user  #Nginx代理服务器的HTTP服务无用户名。
        #http.proxy.password=password  #Nginx代理服务器的HTTP服务无用户密码。
        ```

    4.  按Esc键，输入:wq，再按Enter键，保存并退出文件agent.properties。

    5.  执行以下命令，重启云监控插件。

        ./cloudmonitorCtl.sh restart


## 步骤三：查看非阿里云主机的监控数据

1.  登录[云监控控制台](https://cloudmonitor.console.aliyun.com)。

2.  在左侧导航栏，单击**主机监控**。

3.  在主机监控的实例列表页签，单击目标主机的实例名称链接，或单击目标主机对应**操作**列的**监控图表**。

    查看非阿里云主机的监控数据。


