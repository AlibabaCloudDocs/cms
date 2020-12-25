# Create an application group

The application group feature allows you to manage resources from different services and regions by group. You can create application groups based on your business requirements. You can add resources such as servers and databases related to the same business to an application group, and manage alert rules by application group.

The following table describes the methods of creating application groups and the Alibaba Cloud services that are supported by each creation method.

|Creation method|Description|Supported Alibaba Cloud services|
|---------------|-----------|--------------------------------|
|**Standard group creation**|You can create a standard application group to manage existing instances based on your business requirements.|[Supported Alibaba Cloud services](/intl.en-US/Appendix 1: Metrics/Overview.md)|
|**Smart tag synchronization-based creation**|If tags are attached to your instances, you can specify a tag-based matching rule to create an application group. All instances that match the rule are automatically added to the application group for you to manage. An application group is automatically created for a tag of the existing instances if the tag is specified in the matching rule. If a newly created instance has a tag that is specified in the matching rule, an application group is also automatically created for the tag. Up to 3,000 instances can match a rule at a time.For more information about how to create and attach tags in Resource Management, see [Create and bind a tag]().

|-   Elastic Compute Service \(ECS\)
-   ApsaraDB RDS
-   Server Load Balancer \(SLB\) |
|**Smart instance rule-based creation**|You can specify an instance name-based matching rule to create an application group. All instances that match the rule are automatically added to the application group for you to manage.|-   ECS
-   ApsaraDB RDS
-   SLB
-   ApsaraDB for Redis of the cluster edition
-   ApsaraDB for Redis of the standard edition
-   ApsaraDB for Redis of the read/write splitting edition
-   ApsaraDB for MongoDB
-   ApsaraDB for MongoDB of the sharded cluster architecture |
|**Resource group-based creation**|If you have specified a resource group, you can create an application group from the resource group. All instances in the resource group are added to the application group for you to manage.For more information about how to create resource groups in Resource Management, see [Create a resource group]().

|-   ECS
-   ApsaraDB RDS
-   SLB
-   Elastic IP Address \(EIP\)
-   Anti-DDoS Premium and Anti-DDoS Pro
-   Alibaba Cloud CDN
-   EIP Bandwidth Plan
-   PolarDB
-   ApsaraDB for Redis |

## Create a standard application group

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Application Groups**.

3.  On the Application grouping tab, click **Create Group** in the upper-right corner.

4.  In the Create Group panel, set the **Creation method** parameter to **Standard Group creation** and set other parameters.

    |Parameter|Description|
    |---------|-----------|
    |**Basic Information**|Set the Product Group Name and Contact Group parameters. Valid values:     -   **Product Group Name**: the name of the application group.
    -   **Contact Group**: the alert group to which alert notifications are sent. You can select an existing alert group or create an alert group. |
    |**MonitorAlert**|Set the Select Template and Muted parameters. Valid values:    -   **Select Template**: the alert template used to initialize alert rules of the application group.

For more information about how to create an alert template, see [Create an alert template](/intl.en-US/Alarm service/Alert templates/Create an alert template.md).

    -   **Muted**: the interval of re-sending the notification for an alert before the alert is cleared. The minimum value is 5 minutes and the maximum value is 24 hours. |
    |**Initialize Agent Installation**|After you turn on **Initialize Agent Installation**, Cloud Monitor automatically installs the Cloud Monitor agent on the instances in the application group to collect monitoring data from the instances.|
    |**Event Monitor**|If you select **Subscribe Event notification**, Cloud Monitor automatically sends alert notifications to you when critical or warning events occur on the instances added to the application group.|

5.  Click **Create Group**.

6.  On the Application grouping tab, select Custom to view the application group.


## Create an application group based on smart tag synchronization

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Application Groups**.

3.  On the Application grouping tab, click **Create Group** in the upper-right corner.

4.  In the Create Group panel, set the **Creation method** parameter to **Smart tag synchronization creation** and set other parameters.

    |Parameter|Description|
    |---------|-----------|
    |**Basic Information**|Set the Product Group Name and Contact Group parameters. Valid values:     -   **Product Group Name**: Cloud Monitor automatically generates a name for the application group.
    -   **Contact Group**: the alert group to which alert notifications are sent. You can select an existing alert group or create an alert group. |
    |**MonitorAlert**|Select alert templates. You can initialize alert rules of the application group by using the alert templates.For more information about how to create an alert template, see [Create an alert template](/intl.en-US/Alarm service/Alert templates/Create an alert template.md). |
    |**Region**|The region where the application group resides.|
    |**Match Rule**|You can specify a dynamic matching rule based on a resource tag to automatically add instances. Valid values:    -   **Resource Tag Key**: the key of the instance tag.
    -   **Tag Value**: the value of the instance tag. Instances whose tag values **contain**, **start with**, **end with**, **do not contain**, or **equal to** the value you specify are automatically added to the application group. If you set the Tag Value parameter to **All**, all instances with the specified tag are added to the application group. A newly created instance that matches the rule will also be added to the application group. |
    |**Initialize Agent Installation**|After you turn on **Initialize Agent Installation**, Cloud Monitor automatically installs the Cloud Monitor agent on the instances in the application group to collect monitoring data from the instances.|
    |**Event Monitor**|If you select **Subscribe Event notification**, Cloud Monitor automatically sends alert notifications to you when critical or warning events occur on the instances added to the application group.|

5.  Click **Add**.

6.  On the Application grouping tab, select **Resource tags** from the drop-down list and view the created application group.


## Create an application group based on a smart instance rule

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Application Groups**.

3.  On the Application grouping tab, click **Create Group** in the upper-right corner.

4.  In the Create Group panel, set the **Creation method** parameter to **Smart Instance Rule Creation** and set other parameters.

    |Parameter|Description|
    |---------|-----------|
    |**Basic Information**|Set the Product Group Name and Contact Group parameters. Valid values:     -   **Product Group Name**: the name of the application group.
    -   **Contact Group**: the alert group to which alert notifications are sent. You can select an existing alert group or create an alert group. |
    |**MonitorAlert**|Set the Select Template and Muted parameters. Valid values:    -   **Select Template**: the alert template used to initialize alert rules of the application group.

For more information about how to create an alert template, see [Create an alert template](/intl.en-US/Alarm service/Alert templates/Create an alert template.md).

    -   **Muted**: the interval of re-sending the notification for an alert before the alert is cleared. The minimum value is 5 minutes and the maximum value is 24 hours. |
    |**Add Instance dynamically**|Specify the matching rule so that Cloud Monitor automatically adds instances to the application group based on the name of the instances.|
    |**Initialize Agent Installation**|After you turn on **Initialize Agent Installation**, Cloud Monitor automatically installs the Cloud Monitor agent on the instances in the application group to collect monitoring data from the instances.|
    |**Event Monitor**|If you select **Subscribe Event notification**, Cloud Monitor automatically sends alert notifications to you when critical or warning events occur on the instances added to the application group.|

5.  Click **Create Group**.

6.  On the Application grouping tab, select Custom to view the application group.


## Create an application group from a resource group

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Application Groups**.

3.  On the Application grouping tab, click **Create Group** in the upper-right corner.

4.  In the Create Group panel, set the **Creation method** parameter to **Resource group creation** and set other parameters.

    |Parameter|Description|
    |---------|-----------|
    |**Basic Information**|Set the Resource group creation and Contact Group parameters. Valid values:     -   **Resource group creation**: Select a resource group that was created in the Resource Management console.
    -   **Contact Group**: the alert group to which alert notifications are sent. You can select an existing alert group or create an alert group. |
    |**Initialize Agent Installation**|After you turn on **Initialize Agent Installation**, Cloud Monitor automatically installs the Cloud Monitor agent on the instances in the application group to collect monitoring data from the instances.|
    |**Event Monitor**|If you select **Subscribe Event notification**, Cloud Monitor automatically sends alert notifications to you when critical or warning events occur on the instances added to the application group.|

5.  Click **Add**.

6.  On the Application grouping tab, select **Resource group** from the drop-down list and view the created application group.


-   [Add resources to an application group](/intl.en-US/Application groups/Add resources to an application group.md)
-   [Apply an alert template to an application group](/intl.en-US/Application groups/Apply an alert template to an application group.md)

