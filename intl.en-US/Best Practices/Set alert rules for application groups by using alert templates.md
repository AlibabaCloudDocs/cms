# Set alert rules for application groups by using alert templates

If your Alibaba Cloud account has a large number of cloud resources, you can manage these cloud resources by using application groups. To set the same alert rule for multiple application groups, you can create an alert template.

This topic describes how to set alert rules for Elastic Compute Service \(ECS\), ApsaraDB RDS, and Server Load Balancer \(SLB\) instances by using alert templates and application groups. This way, a Cloud Monitor alert system is created.

1.  Create an alert contact.

    1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

    2.  In the left-side navigation pane, choose **Alerts** \> **Alert Contacts**.

    3.  On the Alert Contacts tab of the Alert Contacts page, click **Create Alert Contact**.

    4.  In the Set Alert Contact pane,set the Name, Email ID, DingTalk Robot, and Alert Notification Information Language parameters.

    5.  Verify the parameters and then click **OK**.

2.  Create an alert contact group. For example, you can create a group named InventoryManagementAlertGroup.

    1.  On the Alert Contacts page, click the **Alert Contact Group** tab.

    2.  On the Alert Contact Group tab, click **Create Alert Contact Group**.

    3.  In the Create Alert Contact Group pane, specify the contact group name and add alert contacts to the group.

    4.  Click **Confirm**.

3.  Create an application group. For example, you can create an application group named InventoryManagementOnlineEnvironment.

    1.  In the left-side navigation pane, choose **Application Groups**.

    2.  On the Application Groups page, click **Create Group** in the upper-right corner.

    3.  In the Create Group pane, set the **Creation Method** parameter to **Smart Instance Rule Creation**, the **Application Group Name** parameter to **InventoryManagementOnlineEnvironment**, and the **Contact Group** parameter to **InventoryManagementAlertGroup**. Then, set the Match Rule parameter for ECS, ApsaraDB RDS, and SLB instances.

        ![Create an application group](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/5172199061/p189908.png)

    4.  Click **Create Application Group**.

4.  Create an alert template and apply it to an application group. For example, you can create an alert template named E-commerceBackgroundModuleTemplate.

    1.  In the left-side navigation pane, choose **Alerts** \> **Alert Templates**.

    2.  On the Alert Templates page, click **Create Alert Template** in the upper-right corner.

    3.  In the Create/modify alert templates pane, set the **Template Name** parameter to **E-commerceBackgroundModuleTemplate**, and then set alert rules for ECS, ApsaraDB RDS, and SLB instances.

        ![Basic information](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/5172199061/p189863.png)

    4.  Click **OK**.

    5.  In the Create/modify alert template complete dialog box, click **OK**.

    6.  In the Apply Template to Group dialog box, select the **InventoryManagementOnlineEnvironment** application group. Set the **Muted**, **Effective Period**, **HTTP Callback**, and **Option** parameters.

    7.  Click **OK**.

    8.  In the Apply Template to Group dialog box, click **OK**.

5.  View the health status of instances that match the alert rules in the application group.

    1.  In the left-side navigation pane, choose **Application Groups**.

    2.  On the **Application grouping** tab, find the application group and click its name or ID in the **Group Name / Group ID** column.

    3.  In the Group Instances section, view the health status of the instances.

        If no alerts are triggered based on the alert rules that are created for the instances, the **Health Status** parameter is **OK**. If an alert is triggered, the **Health Status** parameter is **Alert Status**.


