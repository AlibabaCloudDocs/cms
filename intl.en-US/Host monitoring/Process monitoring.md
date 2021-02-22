# Process monitoring

By default, process monitoring allows you to collect information about active processes, including the CPU usage, memory usage, and number of opened files during a time period. If you add a process keyword, you can collect the number of processes that match the keyword.

The Cloud Monitor agent is installed on the host. For more information, see [Install and uninstall the Cloud Monitor agent](/intl.en-US/Host monitoring/Cloud Monitor agent/Install and uninstall the Cloud Monitor agent.md).

-   The Cloud Monitor agent collects the top five processes with the most CPU consumption every minute. This agent also records the CPU usage, memory usage, and number of opened files in these processes.
    -   CPU usage and memory usage of a process

        For more information about the two metrics, see the top command in the Linux operating system.

    -   Number of opened files in a process

        For more information of this metric, see the lsof command in the Linux operating system.

-   If your process occupies multiple CPU cores, the collected CPU usage may exceed 100%. This is because the Cloud Monitor agent collects the total CPU usage of the process on all the occupied CPU cores.
-   If the top five processes vary during the time period specified in your query, the process list displays all the processes that have ranked top five over the specified time period. The time displayed in the list indicates when the processes last ranked top five.
-   The Cloud Monitor agent only collects the CPU usage, memory usage, and number of opened files for a process when the process ranks top five. If a process has not stayed in top five within the time period specified in your query, its monitoring data is displayed as dispersed data points in the monitoring charts. The density of the data points indicates the activity level of the process on the host. The following figures show examples:
    -   In the following figures, the data points for the wrapper process are sparse and discontinuous in the monitoring charts. This is because the wrapper process did not continuously rank top five with the most CPU consumption during the specified time period.
    -   In the following figures, the data points for the java process are dense and continuous in the monitoring charts. This is because the java process continuously ranked top five with the most CPU consumption during the specified time period.

## Add a process

You can monitor the number and status of key processes by adding process keywords.

Assume that the following processes run on your host:

-   `/usr/bin/java -Xmx2300m -Xms2300m org.apache.catalina.startup.Bootstrap`
-   `/usr/bin/ruby`
-   `nginx -c /ect/nginx/nginx.conf`

You can add the following process keywords and obtain the following monitoring results:

-   `ruby`: One process matches this keyword by name. Therefore, the number of the processes that match this keyword is 1.
-   `nginx`: One process matches this keyword by name and parameter. Therefore, the number of the processes that match this keyword is 1.
-   `/usr/bin`: Two processes match this keyword by path. Therefore, the number of the processes that match this keyword is 2.
-   `apache.catalina`: One process matches this keyword by parameter. Therefore, the number of the processes that match this keyword is 1.
-   `nginx.conf`: One process matches this keyword by parameter. Therefore, the number of the processes that match this keyword is 1.
-   `-c`: One process matches this keyword by parameter. Therefore, the number of the processes that match this keyword is 1.

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Host Monitoring**.

3.  On the Instances tab of the Host Monitoring page, find the host, and click its name or click **Monitoring Charts** in the **Actions** column.

4.  On the Instance Info page, click the **Process Monitoring** tab.

5.  On the Process Monitoring tab, click **Add Process** in the upper-right corner.

6.  In the Add Process Monitor dialog box, enter a process name and click **Add**.

7.  Click **Close**.


## Delete the process

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Host Monitoring**.

3.  On the Instances tab of the Host Monitoring page, find the host, and click its name or click **Monitoring Charts** in the **Actions** column.

4.  On the Instance Info page, click the **Process Monitoring** tab.

5.  On the Process Monitoring tab, click **Add Process** in the upper-right corner.

6.  In the Add Process Monitor dialog box, click **Delete** in the **Actions** column to delete the process.

7.  Click **Close**.


## Configure an alert rule for a process

After you add a process, you can configure an alert rule for the process. You can then receive alert notifications if the number of processes that match the process keyword changes.

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Host Monitoring**.

3.  On the Host Monitoring page, click the **Alert Rules** tab.

4.  On the Alert Rules tab, click **Create Alert Rule**.

5.  On the Create Alert Rule page, select **Host Process Number** from the **Rule Description** drop-down list. Set other parameters of the alert rule based on your business requirements.

    -   If multiple processes run on the host and the number of processes that matches each process keyword varies, you can click **Add Alarm Rule** to configure multiple alert rules at a time.
    -   For information about how to set parameters of an alert rule, see [Create a threshold-triggered alert rule](/intl.en-US/Alarm service/Alarm rules/Create a threshold-triggered alert rule.md).
6.  Click **Confirm**.


