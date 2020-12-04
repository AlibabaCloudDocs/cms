# Host monitoring

Host monitoring collects multiple monitoring data of operating system metrics from your hosts by using the Cloud Monitor agents installed on your hosts.

Scenarios

-   Monitor hosts in a hybrid cloud

    Cloud Monitor collects monitoring data from your hosts by using the Cloud Monitor agents installed on your hosts. You can install the Cloud Monitor agent on both Alibaba Cloud Elastic Compute Service \(ECS\) instances and non-ECS hosts to collect monitoring data from hosts in a hybrid cloud.

-   Monitor hosts of an enterprise

    Host monitoring allows you to group hosts in different regions to an application group for business-based host management. In addition, host monitoring allows you to manage alert rules by application group. You can apply one alert rule to all hosts of an application group. This improves the O&M efficiency and overall management experience.


## Install Cloud Monitor agents

1.  Log on to the [Cloud Monitor console](https://cloudmonitor.console.aliyun.com).

2.  In the left-side navigation pane, click **Host Monitoring**.

3.  On the Instances tab of the Host Monitoring page, select the hosts on which you want to install or upgrade the Cloud Monitor agent.

4.  Click **Batch Install**.

    Wait for about 5 minutes. When the **agent status** changes from **Installing** to **Running**, the installation or upgrade is successful.

5.  Turn on **New purchase ECS automatically installs Cloud Monitor**.

    After you turn on this switch, the Cloud Monitor agent is automatically installed on new ECS instances. Otherwise, you must manually install the agent.


## View monitoring charts

1.  Log on to the[Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Host Monitoring**.

3.  On the Instances tab of the Host Monitoring page, click the instance name of the host or click **Monitoring Charts** in the **Actions** column.

4.  On the instance details page, you can view the monitoring charts of the key metrics of your host.


## Configure an alert rule

