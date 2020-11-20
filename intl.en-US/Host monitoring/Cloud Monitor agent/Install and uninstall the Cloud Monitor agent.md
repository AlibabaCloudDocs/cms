# Install and uninstall the Cloud Monitor agent

This topic describes how to automatically install, manually install, and uninstall the C++ agent of Cloud Monitor.

## Automatically install the Cloud Monitor agent \(Recommended\)

Perform the following steps to enable automatic installation of the Cloud Monitor agent on Elastic Compute Service \(ECS\) instances provided by Alibaba Cloud and hosts that are not provided by Alibaba Cloud:

1.  Log on to the [Cloud Monitor console](https://cloudmonitor.console.aliyun.com).

2.  In the left-side navigation pane, click **Host Monitoring**.

3.  On the Instances tab of the Host Monitoring page, select the hosts on which you want to install or upgrade the Cloud Monitor agent.

4.  Click **Batch Install**.

    Wait for about 5 minutes. When the **agent status** changes from **Installing** to **Running**, the installation or upgrade is successful.

5.  Turn on **New purchase ECS automatically installs Cloud Monitor**.

    After you turn on this switch, the Cloud Monitor agent is automatically installed on new ECS instances. Otherwise, you must manually install the agent.


## Manually install the Cloud Monitor agent on ECS instances

**Note:** If you have installed the Java or GoLang agent on the ECS instance, uninstall the Java or GoLang agent first. For more information, see [How do I uninstall the Java agent or GoLang agent of Cloud Monitor?](/intl.en-US/FAQ/Operation/How do I uninstall the Java agent or GoLang agent of Cloud Monitor?.md)

1.  Log on to the [Cloud Monitor console](https://cloudmonitor.console.aliyun.com).

2.  In the left-side navigation pane, click **Host Monitoring**.

3.  On the Instances tab of the Host Monitoring page, click **Aliyun ECS install** in the upper-right corner.

4.  In the Monitor Install Guide panel, select the region and operating system of the ECS instance. Then, copy and run the commands that are displayed in the panel as prompted to install the Cloud Monitor agent.

    -   Windows

        ![Windows ECS instances](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/6137132061/p165759.png)

        1.  Download the agent package of the 32-bit version or 64-bit version based on the operating system of the ECS instance.
        2.  Log on to the ECS instance on which you want to install the Cloud Monitor agent as the administrator.
        3.  Create a directory named cloudmonitor in the C:\\Program Files\\Alibaba directory.
        4.  Upload the agent package to the ECS instance and decompress the agent package to the C:\\Program Files\\Alibaba\\cloudmonitor directory.
        5.  Open Command Prompt.

            Press Win+R. In the Run dialog box, enter cmd and click **OK**.

        6.  Run the following commands to install the Cloud Monitor agent:

            cd C:\\Program Files\\Alibaba\\cloudmonitor\\bin

            argusagent\_service.exe install

        7.  Run the following command to start the Cloud Monitor agent:

            net start argusagent

        8.  Query the status of the Cloud Monitor agent.
            1.  Open the Services window.

                Press Win+R. In the Run dialog box, enter services.msc and click **OK**.

            2.  View the status of the **argusagent** service.

                If the status of the argusagent service is **Running**, the Cloud Monitor agent is properly running.

    -   Linux

        ![Linux ECS instances](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/6137132061/p165763.png)

        1.  In the Monitor Install Guide panel, click **Click the copy installation command**.
        2.  Log on to the ECS instance on which you want to install the Cloud Monitor agent as the root user.
        3.  Paste and run the command to install the Cloud Monitor agent.
        4.  Run the following command to view the status of the Cloud Monitor agent:

            ps aux \| grep argusagent \| grep -v grep

            The following output indicates that the Cloud Monitor agent is properly running:

            ```
            root      2284  0.0  0.0  22516  1488 ?        Ss   Sep14   0:00 /usr/local/cloudmonitor/bin/argusagent -d
            root      2286  0.2  0.3 939652 14300 ?        Sl   Sep14   3:15 /usr/local/cloudmonitor/bin/argusagent
            ```


## Manually install the Cloud Monitor agent on hosts that are not provided by Alibaba Cloud

**Note:** If you have installed the Java or GoLang agent on the host, uninstall the Java or GoLang agent first. For more information, see [How do I uninstall the Java agent or GoLang agent of Cloud Monitor?](/intl.en-US/FAQ/Operation/How do I uninstall the Java agent or GoLang agent of Cloud Monitor?.md)

1.  Log on to the [Cloud Monitor console](https://cloudmonitor.console.aliyun.com).

2.  In the left-side navigation pane, click **Host Monitoring**.

3.  On the Instances tab of the Host Monitoring page, click **Not Aliyun ecs install** in the upper-right corner.

4.  In the Monitor Install Guide panel, select the region and operating system of the host. Then, copy and run the commands that are displayed in the panel as prompted to install the Cloud Monitor agent.

    -   Windows

        ![Windows hosts](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/6137132061/p165767.png)

        1.  Download the agent package of the 32-bit version or 64-bit version based on the operating system of the host.
        2.  Download the accesskey.properties configuration file.
        3.  Log on to the host on which you want to install the Cloud Monitor agent as the administrator.
        4.  Create a directory named cloudmonitor in the C:\\Program Files\\Alibaba directory.
        5.  Upload the agent package to the host and decompress the agent package to the C:\\Program Files\\Alibaba\\cloudmonitor directory.
        6.  Upload the configuration file to the C:\\Program Files\\Alibaba\\cloudmonitor\\local\_data\\conf directory of the host.
        7.  Open the command prompt window.

            Press Win+R. In the Run dialog box, enter cmd and click **OK**.

        8.  Run the following command to install the Cloud Monitor agent:

            cd C:\\Program Files\\Alibaba\\cloudmonitor\\bin

            argusagent\_service.exe install

        9.  Run the following command to start the Cloud Monitor agent:

            net start argusagent

        10. Query the status of the Cloud Monitor agent.
            1.  Open the Services window.

                Press Win+R. In the Run dialog box, enter services.msc and click **OK**.

            2.  View the status of the **argusagent** service.

                If the status of the argusagent service is **Running**, the Cloud Monitor agent is properly running.

    -   Linux

        ![Linux hosts](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/6137132061/p165768.png)

        1.  On the monitoring installation guide page, click **click copy installation command**.
        2.  Log on to the host on which you want to install the Cloud Monitor agent as the root user.
        3.  Paste and run the command to install the Cloud Monitor agent.
        4.  Run the following command to view the status of the Cloud Monitor agent:

            ps aux \| grep argusagent \| grep -v grep

            The following output indicates that the Cloud Monitor agent is properly running:

            ```
            root      2284  0.0  0.0  22516  1488 ?        Ss   Sep14   0:00 /usr/local/cloudmonitor/bin/argusagent -d
            root      2286  0.2  0.3 939652 14300 ?        Sl   Sep14   3:15 /usr/local/cloudmonitor/bin/argusagent
            ```


## Uninstall the Cloud Monitor agent

After you uninstall the Cloud Monitor agent from a host, you cannot monitor the host in real time in the Cloud Monitor console, but you can view the historical metric data.

-   Windows
    1.  Log on to the host where the Cloud Monitor agent resides as the administrator.
    2.  Open the command prompt window.

        Press Win+R. In the Run dialog box, enter cmd and click **OK**.

    3.  Run the following command to stop the Cloud Monitor agent:

        net stop argusagent

    4.  Run the following command to uninstall the Cloud Monitor agent:

        "C:\\Program Files\\Alibaba\\cloudmonitor\\bin\\argusagent\_service.exe" uninstall

    5.  Run the following command to delete the cloudmonitor directory:

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


