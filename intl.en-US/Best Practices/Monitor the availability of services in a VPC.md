# Monitor the availability of services in a VPC

This topic describes how to use Cloud Monitor to monitor the availability of services in a virtual private cloud \(VPC\).

## Background information

As an increasing number of users migrate their services from the classic network to VPCs that are safer and more reliable, users need to monitor the availability of services in VPCs. This topic describes how to monitor the availability of services in a VPC, including Elastic Compute Service \(ECS\), ApsaraDB RDS, ApsaraDB for Redis, and Server Load Balancer \(SLB\).

## Preparations

The following figure shows how to monitor the availability of services in a VPC.

![Monitor services in a VPC](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/2430287951/p5495.png)

Before you can monitor the availability of services in a VPC, you must install the Cloud Monitor agent on the ECS instances that will be used as monitoring nodes. To monitor the availability of a service in a VPC, create an availability monitoring task in the Cloud Monitor console, select a monitoring node, and specify the URL or port of the monitored target. After you create the availability monitoring task, the Cloud Monitor agent on the monitoring node sends an HTTP request or a Telnet request to the URL or port every minute. The Cloud Monitor agent collects the response time and status codes and reports the monitoring results to Cloud Monitor. Cloud Monitor displays the monitoring results in a chart and generates alerts if the connection times out or the monitoring fails.

## Procedure

**Note:**

-   You must install the Cloud Monitor agent on the ECS instances that will be used as monitoring nodes.
-   You must create an application group and add the monitoring nodes to the group.

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).
2.  In the left-side navigation pane, click **Application Groups**.
3.  On the **Application grouping** tab of the **Application Groups** page, click the name or ID of the application group for which you want to create an availability monitoring task.
4.  In the left-side navigation pane of the page that appears, click **Availability Monitoring**.
5.  On the page that appears, click **Create Configuration** in the upper-right corner.
6.  In the CreateAvailability Monitoring dialog box, set relevant parameters.
    -   To monitor whether local processes on ECS instances in a VPC respond, select the ECS instances to be monitored in the Target Server section, set the Detection Target parameter to URL or IP address, and enter the addresses in localhost:port/path format in the Detection Type section.
    -   To monitor whether an SLB instance in a VPC responds, select an ECS instance that resides in the same VPC as the SLB instance in the Target Server section, set the Detection Target parameter to URL or IP address, and enter the address of the SLB instance in the Detection Type section.
    -   To monitor whether an ApsaraDB RDS or ApsaraDB for Redis instance in a VPC responds to an ECS instance, add the ApsaraDB RDS or ApsaraDB for Redis instance to the application group of the ECS instance, select the ECS instance in the Target Server section, and set the Detection Target parameter to RDS-DB or KVStore for Redis.
7.  Click **OK**.

    You can view the monitoring results in the monitoring chart of the task. If the connection times out or the monitoring fails, you can receive an alert notification.

    ![Availability monitoring list](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/2430287951/p5498.png)

8.  Find the task and click **Monitoring Charts** in the Actions column to view the monitoring details of the task.

    ![Monitoring chart](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/2430287951/p5499.png)


