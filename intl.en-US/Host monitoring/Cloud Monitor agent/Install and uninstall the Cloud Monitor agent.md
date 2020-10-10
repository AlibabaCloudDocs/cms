# Install and uninstall the Cloud Monitor agent

This topic describes how to automatically install, manually install, and uninstall the C++ agent of Cloud Monitor.

## Automatically install the Cloud Monitor agent \(Recommended\)

Perform the following steps to automatically install the Cloud Monitor agent on Elastic Compute Service \(ECS\) instances provided by Alibaba Cloud and hosts not provided by Alibaba Cloud:

1.  Log on to the [Cloud Monitor console](https://cloudmonitor.console.aliyun.com).

2.  In the left-side navigation pane, click **Host Monitoring**.

3.  On the Instances tab of the Host Monitoring page, select the hosts on which you want to install or upgrade the Cloud Monitor agent.

4.  Click **Batch Install**.

    Wait for a while. When the agent status changes from **Installing** to **Running**, the installation or upgrade is successful.


## Manually install the Cloud Monitor agent on ECS instances

If the Java agent or GoLang agent has been installed on the ECS instance where you want to manually install the C++ agent, uninstall the Java agent or GoLang agent first. For more information, see [How do I uninstall the Java agent or GoLang agent of Cloud Monitor?]()

1.  Log on to the [Cloud Monitor console](https://cloudmonitor.console.aliyun.com).

2.  In the left-side navigation pane, click **Host Monitoring**.

3.  On the Instances tab of the Host Monitoring page, click **Aliyun ECS install** in the upper-right corner.

4.  In the Monitor Install Guide pane, select the region and operating system of the ECS instance. Then, copy and run the commands that are displayed in the pane as prompted to install the Cloud Monitor agent.

    -   Windows

        ![ECS instances that run Windows](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/6137132061/p165759.png)

        1.  Download the agent package of the 32-bit version or 64-bit version based on the operating system of the ECS instance.
        2.  Log on to the ECS instance on which you want to install the Cloud Monitor agent as the administrator.
        3.  Create a directory named cloudmonitor in the C:\\Program Files\\Alibaba directory.
        4.  Upload the agent package to the ECS instance and decompress the agent package to the C:\\Program Files\\Alibaba\\cloudmonitor directory.
        5.  Open the command prompt window.

            Press Win+R. In the Run dialog box, enter cmd and click **OK**.

        6.  Run the following commands to install the Cloud Monitor agent:

            cd C:\\Program Files\\Alibaba\\cloudmonitor\\bin

            argusagent\_service.exe install

        7.  Run the following command to start the Cloud Monitor agent:

            net start argusagent

    -   Linux

        ![ECS instances that run Linux](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/6137132061/p165763.png)

        1.  Log on to the ECS instance on which you want to install the Cloud Monitor agent as the root user.
        2.  Run the following command to install the Cloud Monitor agent:

            ARGUS\_VERSION=3.4.7 /bin/bash -c "$\(curl -s https://cms-agent-cn-shanghai.oss-cn-shanghai-internal.aliyuncs.com/Argus/agent\_install\_ecs-1.2.sh\)"


## Manually install the Cloud Monitor agent on hosts not provided by Alibaba Cloud

If the Java agent or GoLang agent has been installed on the host where you want to manually install the C++ agent, uninstall the Java agent or GoLang agent first. For more information, see [How do I uninstall the Java agent or GoLang agent of Cloud Monitor?]()

1.  Log on to the [Cloud Monitor console](https://cloudmonitor.console.aliyun.com).

2.  In the left-side navigation pane, click **Host Monitoring**.

3.  On the Instances tab of the Host Monitoring page, click **Not Aliyun ecs install** in the upper-right corner.

4.  In the Monitor Install Guide pane, select the region and operating system of the host. Then, copy and run the commands that are displayed in the pane as prompted to install the Cloud Monitor agent.

    -   Windows

        ![Hosts not provided by Alibaba Cloud that run Windows](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/6137132061/p165767.png)

        1.  Download the agent package of the 32-bit version or 64-bit version based on the operating system of the host.
        2.  Download the configuration file accesskey.properties.
        3.  Log on to the host on which you want to install the Cloud Monitor agent as the administrator.
        4.  Create a directory named cloudmonitor in the C:\\Program Files\\Alibaba directory.
        5.  Upload the agent package to the host and decompress the agent package to the C:\\Program Files\\Alibaba\\cloudmonitor directory.
        6.  Upload the configuration file to the C:\\Program Files\\Alibaba\\cloudmonitor\\local\_data\\conf directory of the host.
        7.  Open the command prompt window.

            Press Win+R. In the Run dialog box, enter cmd and click **OK**.

        8.  Run the following commands to install the Cloud Monitor agent:

            cd C:\\Program Files\\Alibaba\\cloudmonitor\\bin

            argusagent\_service.exe install

        9.  Run the following command to start the Cloud Monitor agent:

            net start argusagent

    -   Linux

        ![Hosts not provided by Alibaba Cloud that run Linux](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/6137132061/p165768.png)

        1.  Log on to the host on which you want to install the Cloud Monitor agent as the root user.
        2.  Run the following command to install the Cloud Monitor agent:

            CMS\_AGENT\_ACCESSKEY=BIlmZlE\*\*\*\* CMS\_AGENT\_SECRETKEY=kh7bvCh-O\_TLEyVWT2\*\*\*\* ARGUS\_VERSION=3.4.7 /bin/bash -c "$\(curl -s http://cms-download.aliyun.com/Argus/agent\_install\_necs-1.2.sh\)"


## Uninstall the Cloud Monitor agent

-   Windows
    1.  Log on to the host where the Cloud Monitor agent resides as the administrator.
    2.  Open the command prompt window.

        Press Win+R. In the Run dialog box, enter cmd and click **OK**.

    3.  Run the following command to stop the Cloud Monitor agent:

        net stop argusagent

    4.  Run the following command to uninstall the Cloud Monitor agent:

        "C:\\Program Files\\Alibaba\\cloudmonitor\\bin\\argusagent\_service.exe" uninstall

    5.  Run the following commands to delete the cloudmonitor directory:

        cd C:\\Program Files\\Alibaba

        rd /s /q cloudmonitor

-   Linux
    1.  Log on to the host where the Cloud Monitor agent resides as the root user.
    2.  Run the following command to stop the Cloud Monitor agent:

        bash /usr/local/cloudmonitor/cloudmonitorCtl.sh stop

    3.  Run the following command to uninstall the Cloud Monitor agent:

        bash /usr/local/cloudmonitor/cloudmonitorCtl.sh uninstall

    4.  Run the following command to delete the cloudmonitor directory:

        rm -rf /usr/local/cloudmonitor


