# How do I report the monitoring data of hosts that are not provided by Alibaba Cloud to Cloud Monitor by using an NGINX proxy server?

This topic describes how to report the monitoring data of hosts that are not provided by Alibaba Cloud to Cloud Monitor by using an NGINX proxy server.

## Step 1: Deploy an NGINX proxy server

1.  Download the latest installation package of NGINX, for example, **nginx-1.19.6**.

    1.  Go to the [nginx: download](https://nginx.org/en/download.html) page.

    2.  Click **nginx-1.19.6** to download the nginx-1.19.6.tar.gz package.

2.  Install NGINX.

    **Note:** We recommend that you use a Linux server as your proxy server because Cloud Monitor is deployed on a Linux server.

    1.  Upload the nginx-1.19.6.tar.gz package to the specified directory of the proxy server, such as /usr/local.

    2.  Log on to the proxy server as the root user.

    3.  Run the following commands to decompress the nginx-1.19.6.tar.gz package to the nginx-1.19.6 directory:

        cd /usr/local

        tar zxvfnginx-1.19.6.tar.gz

    4.  Run the following commands to initialize NGINX:

        cd nginx-1.19.6

        ./configure

    5.  Run the following command to install NGINX:

        make install

    6.  Run the following command to start NGINX:

        ./nginx

    7.  Check whether NGINX is installed.

        In the address bar of your browser, enter IP address of the proxy server:8080. If the following output is displayed, the installation is successful.

        ![Nginx](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/5882893161/p203666.png)

3.  Configure an NGINX proxy.

    1.  Run the following commands to open the nginx.conf file:

        cd conf

        vi nginx.conf

    2.  Edit the configuration file nginx.conf.

        Append the information about a forward or a reverse proxy at the end of the file nginx.conf. You can configure only one forward proxy or one reverse proxy. Otherwise, the configuration is invalid.

        -   Forward proxy

            If you consider the Internet outside the LAN as a huge resource pool, the clients in the LAN need to access the Internet by using a forward proxy.

            ```
            server {  
                    resolver 192.168.XX.XX;  # The IP address of the proxy server.  
                    listen 80;  
                    location / {  
                        proxy_pass http://$http_host$request_uri;  # The protocol and request URI of the proxy server. 
                    } 
            }
            ```

            **Note:** The forward proxy of Nginx does not support HTTPS.

        -   Reverse proxy

            If the LAN provides resources and services to the Internet, the clients on the Internet need to access resources in the LAN by using a reverse proxy.

            ```
            server {
                    server_name 192.168.XX.XX; # The IP address of the proxy server.
                    listen 80;
                    location / {
                            proxy_pass https://www.aliyun.com; # The URL that the proxy server accesses.
                    }
            }
            ```

    3.  Press the Esc key, enter :wq, and then press the Enter key to save and close the nginx.conf file.

    4.  Run the following command to restart the NGINX proxy server:

        nginx -s reload

    5.  Check whether the NGINX proxy is configured.

        -   Forward proxy

            Run the following command to access a URL. If the URL can be accessed, the NGINX proxy is configured.

            curl -x192.168.XX.XX \(IP address of the proxy server\)http://www.aliyun.com \(Any URL\)

        -   Reverse proxy

            Run the following command. If you can access only the URL specified in the nginx.conf file, the NGINX proxy is configured.

            curl -x192.168.XX.XX \(IP address of the proxy server\)https://www.baidu.com \(Any URL\)


## Step 2: Install and configure the Cloud Monitor agent

1.  Install the Cloud Monitor agent on a host that is not provided by Alibaba Cloud.

    For more information, see [Install and uninstall the Cloud Monitor agent](/intl.en-US/Host monitoring/Cloud Monitor agent/Install and uninstall the Cloud Monitor agent.md).

2.  Configure the NGINX proxy server in the Cloud Monitor agent.

    1.  Log on to the host where the Cloud Monitor agent resides as the root user.

    2.  Run the following commands to open the agent.properties file.

        cd /usr/local/cloudmonitor/conf

        vi agent.properties

    3.  Configure the NGINX proxy server in the configuration file of the Cloud Monitor agent.

        The following code provides an example on how to configure an NGINX proxy server:

        ```
        http.proxy.auto=false
        # Manually configure the proxy
        http.proxy.host=192.168.XX.XX # The IP address of the NGINX proxy server.
        http.proxy.port=8080  # The port of the NGINX proxy server.
        #http.proxy.user=user  # The NGINX proxy server does not require a username for HTTP authentication.
        # http.proxy.password=password # The NGINX proxy server does not require a password for HTTP authentication.
        ```

    4.  Press the Esc key, enter :wq, and then press the Enter key to save and close the agent.properties file.

    5.  Run the following command to restart the Cloud Monitor agent:

        ./cloudmonitorCtl.sh restart


## Step 3: View the monitoring data of the host not provided by Alibaba Cloud

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Host Monitoring**.

3.  On the Instances tab of the Host Monitoring page, click the instance name of the host or click **Monitoring Charts** in the **Actions** column.

    View the monitoring data of the host not provided by Alibaba Cloud.


