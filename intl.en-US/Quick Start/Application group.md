# Application group

This topic describes the scenarios of using application groups, the features of application groups, and how to use application groups.

## Scenarios

-   **Manage resources from the business perspective**

    You can add resources in your account to different application groups based on the business type. Then, you can query monitoring data and alerts from the business perspective.

-   **Perform routine inspection and detect faults**

    After you create application groups, you can use features such as group health check, faulty instance list, and dashboard to monitor resources in application groups. You can inspect resource usage in application groups on a routine basis, locate faulty resources, and identify root causes immediately after you receive alert notifications.

-   **Improve resource usage**

    Application groups allow you to aggregate and display monitoring data from multiple dimensions. You can query monitoring data of an application group or a single instance to identify resources that are most frequently accessed.


## Features

-   Application groups allow you to manage your cloud resources in different services and regions from the business perspective.
-   When you apply an alert rule to an application group, the alert rule is applied to all resources in the application group. This greatly improves the operations and maintenance \(O&M\) efficiency.
-   You can find faulty instances by using the faulty instance list that is provided for each application group.
-   You can customize and view monitoring charts on the dashboard of an application group.

## Procedure

To create an application group, perform the following steps:

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).
2.  In the left-side navigation pane, click **Application Groups**.
3.  On the Application grouping tab of the Application Groups page, click **Create Group** in the upper-right corner. The Create Group panel appears.
4.  In the **Basic Information** section, enter the application group name and select an alert group.
5.  Optional. In the **MonitorAlert** section, select an alert template to initialize alert rules for the instances in the application group and set the **Muted** parameter. If you turn on **Initialize Agent Installation**, Cloud Monitor installs the Cloud Monitor agent on all instances in the application group.
6.  In the **Event Monitor** section, select the **Subscribe Event notification** check box. When critical and warning events occur on the instances added to the application group, Cloud Monitor sends alert notifications.
7.  In the **Add Instance dynamically** section, configure the rules for dynamically adding Elastic Compute Service \(ECS\) instances. All instances that match the rules are added to the application group. You can click **Add Product** to configure rules for dynamically adding ApsaraDB RDS and Server Load Balancer \(SLB\) instances. You can add instances of other Alibaba Cloud services to the application group after the application group is created.
8.  Click **Create Group**. The application group is created.

