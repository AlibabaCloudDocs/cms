# Create an application group

The application group feature allows you to manage resources from different services and regions by group. You can add your cloud resources, such as business-related servers and databases, to application groups. Then, you can manage alert rules by application group. This topic describes how to create an application group.

You can create an application group in one of the following two modes:

-   Dynamic mode

    When you create an application group, you can specify a name-based matching rule for instances. Instances that match the rule are automatically added to the application group. If you need to add instances to or remove instances from the application group, you only need to change the instance names. The dynamic mode is supported only for Elastic Compute Service \(ECS\), ApsaraDB RDS, and Server Load Balancer \(SLB\) instances.

-   Static mode

    When you create an application group, you manually add instances to the application group.


1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Application Groups**.

3.  On the Application Groups page, click **Create Group** in the upper-right corner.

4.  In the Create Group panel, set the parameters in the **Creation method**, **Basic Information**, **MonitorAlert**,**Region**, **Match Rule**, and **Event Monitor** sections.

    |GUI element|Description|
    |-----------|-----------|
    |**Creation method**|Select the method used to create the application group. Valid values:     -   **Smart tag synchronization creation**
    -   **Standard Group creation**
    -   **Smart Instance Rule Creation** |
    |**Basic Information**|Set the Product Group Name and Contact Group parameters.     -   **Product Group Name**: the name of the application group.

If you select **Smart tag synchronization creation** for **Creation method**, the system automatically generates a name for the application group. If you select **Standard Group creation** or **Smart Instance Rule Creation** for **Creation method**, you must enter a name for the application group.

    -   **Contact Group**: the alert group to which alert notifications are sent. You can customize alert groups based on business needs. |
    |**MonitorAlert**|Set the Select Template and Muted parameters.    -   **Select Template**: the alert template used to initialize alert rules of the application group.
    -   **Muted**: the interval of re-sending the notification for an alert before the alert is cleared. The minimum value is 5 minutes and the maximum value is 24 hours.

The Muted parameter is available only when you select **Standard Group creation** or **Smart Instance Rule Creation** for **Creation method**. |
    |**Region**|Select the region to which the application group belongs. The Region section is available only when you select **Smart tag synchronization creation** for **Creation method**.|
    |**Match Rule**|Specify the matching rule to automatically add instances. All your instances, including those that have not been created, whose names contain, start with, or end with the words you specify will be automatically added to the application group. Only ECS, ApsaraDB RDS, and SLB instances can be added to the application group based on the matching rule that you specify.

The Match Rule section is available only when you select **Smart Instance Rule Creation** for **Creation method**. |
    |**Add Instance dynamically**|Specify the matching rule to automatically add instances.The Add Instance dynamically section is available only when you select **Smart Instance Rule Creation** for **Creation method**. |
    |**Initialize Agent Installation**|If you turn on **Initialize Agent Installation**, Cloud Monitor automatically installs the Cloud Monitor agent on all instances in the application group.|
    |**Event Monitor**|If you select Subscribe Event notification, Cloud Monitor automatically sends alert notifications to you when critical or warning events occur on the instances added to the application group.|

5.  Click **Create Group** or **Add**.

    -   If you select **Standard Group creation** or **Smart Instance Rule Creation** for **Creation method**, click **Create Group**.
    -   If you select **Smart tag synchronization creation** for **Creation method**, click **Add**.

-   [Add resources to an application group](/intl.en-US/Application groups/Add resources to an application group.md)
-   [Apply an alert template to an application group](/intl.en-US/Application groups/Apply an alert template to an application group.md)

