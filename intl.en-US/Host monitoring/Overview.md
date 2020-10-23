# Overview

The host monitoring feature of Cloud Monitor monitors your hosts by using the Cloud Monitor agent that is installed on the hosts. Host monitoring can monitor hosts that run the Linux and Windows operating systems.

## Scenarios

You can use host monitoring to monitor servers or physical machines that are not provided by Alibaba Cloud and Alibaba Cloud Elastic Compute Service \(ECS\) instances.

Host monitoring uses the Cloud Monitor agent that is installed on your hosts to collect a wide range of operating system-related metrics. Host monitoring enables you to monitor the usage of host resources and use the monitoring data for troubleshooting.

## Monitor hosts in a hybrid cloud

Host monitoring uses the Cloud Monitor agent to collect monitoring data from hosts. You can install the Cloud Monitor agent on both Alibaba Cloud ECS instances and non-ECS hosts. This way, you can collect monitoring data from hosts in a hybrid cloud.

## Monitor hosts of an enterprise

Host monitoring allows you to group hosts in different regions to an application group for business-based host management. In addition, host monitoring allows you to manage alert rules by application group. After you apply an alert rule to an application group, the alert rule is applied to all hosts in the application group. This improves the operations and maintenance \(O&M\) efficiency and overall management experience.

**Note:**

-   Host monitoring can monitor hosts that run the Linux and Windows operating systems. It cannot monitor hosts that run the UNIX operating system.
-   To install the Cloud Monitor agent in Linux, you must have the root permissions. To install the Cloud Monitor agent in Windows, you must have the administrator permissions.
-   The Cloud Monitor agent collects the status of TCP connections by running a command similar to the netstat -anp command that is used in Linux. If a large number of TCP connections exist, the Cloud Monitor agent consumes much CPU time to collect the status of the TCP connections. Therefore, the feature of collecting the status of TCP connections is disabled by default. To enable the feature, perform the following steps:

    a. In Linux, change the value of the `netstat.tcp.disable` parameter to `False` in the cloudmonitor/config/conf.properties configuration file. Restart the agent after you modify the configuration.

    b. In Windows, change the value of the `netstat.tcp.disable` parameter to `False` in the C:\\Program Files\\Alibaba\\cloudmonitor\\config configuration file. Restart the agent after you modify the configuration.


## Monitoring capabilities

Host monitoring collects monitoring data of more than 30 [metrics](/intl.en-US/Host monitoring/Metrics.md), including the metrics related to CPU, memory, disk, and network usage. This satisfies your basic requirements on monitoring and O&M of servers.

## Alert capabilities

Host monitoring provides the alert service for all metrics. You can configure alert rules for an instance, an application group, or all resources based on your business needs.

You can apply alert rules to hosts, or add hosts to an application group and apply alert rules to the application group.

