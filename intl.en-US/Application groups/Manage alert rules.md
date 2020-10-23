# Manage alert rules

You can create, view, modify, delete, enable, and disable alert rules for an application group.

An application group is created. For more information, see [Create an application group](/intl.en-US/Application groups/Create an application group.md).

After you select an application group, you can view only the alert rules applied to the application group, not the alert rules applied to a specific instance or all resources.

## Create a threshold-triggered alert rule

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Application Groups**.

3.  On the **Application grouping** tab of the **Application Groups** page, find the application group for which you want to create an alert rule and click its name or ID.

4.  On the Group Resource page, click **Threshold Alert** in the upper-right corner.

5.  In the **Add or Edit Rules** panel, set the parameters in the Product Type, Rule, Alert mechanism, and Contact Group sections.

    -   If you select **Auto Scaling**, you need to set the **Region**, **ESS Group**, and **ESS Rule** parameters. When an alert is triggered, the application group is scaled based on the specified scaling rule.
    -   If you select **Log Service**, you need to set the **Region**, **Project**, and **Logstore** parameters. When an alert is triggered, the alert information is written to the specified Logstore.
6.  Click **Add**.


## Delete an alert rule

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Application Groups**.

3.  On the **Application grouping** tab of the **Application Groups** page, find the application group for which you want to delete an alert rule and click its name or ID.

4.  In the left-side navigation pane, click **Alert Rule**.

5.  Delete a specific alert rule for the application group.

    -   Delete a threshold-triggered or custom event-triggered alert rule
        1.  On the **Threshold Value Alert** tab of the Alert Rule page, find the alert rule that you want to delete and click **Delete** in the **Actions** column.
        2.  In the Delete Alert message, click **OK**.
    -   Delete a system event-triggered alert rule
        1.  Click the **Event Alert** tab.
        2.  On the **Event Alert** tab of the Alert Rule page, find the system event-triggered alert rule that you want to delete and click **Delete** in the **Actions** column.
        3.  In the Delete Alert message, click **OK**.

## Modify an alert rule

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Application Groups**.

3.  On the **Application grouping** tab of the **Application Groups** page, find the application group for which you want to modify an alert rule and click its name or ID.

4.  In the left-side navigation pane, click **Alert Rule**.

5.  Modify an alert rule.

    -   Modify a threshold-triggered alert rule
        1.  On the **Threshold Value Alert** tab of the Alert Rule page, find the threshold-triggered alert rule that you want to modify and click **Modify** in the **Actions** column.
        2.  In the Add or Edit Rules panel, modify parameters as required.
        3.  Click **Add**.
    -   Modify a custom event-triggered alert rule
        1.  On the **Threshold Value Alert** tab of the Alert Rule page, find the custom event-triggered alert rule that you want to modify and click **Modify** in the **Actions** column.
        2.  In the Create / Modify Event Alert panel, modify parameters as required.
        3.  Click **OK**.
    -   Modify a system event-triggered alert rule
        1.  Click the **Event Alert** tab.
        2.  On the **Event Alert** tab of the Alert Rule page, find the system event-triggered alert rule that you want to modify and click **Modify** in the **Actions** column.
        3.  In the Create / Modify Event Alert panel, modify parameters as required.
        4.  Click **OK**.

## Disable or enable all alert rules for an application group

If you need to manually stop a service for maintenance or upgrade, you can disable all alert rules for the application group to which resources of the service belong. This way, you can prevent the system from generating a large number of unwanted alert notifications when the service is stopped. After you maintain or upgrade the service, you can enable all alert rules for the application group.

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Application Groups**.

3.  On the Application grouping tab of the **Application Groups** page, disable or enable all alert rules for an application group.

    -   Disable all alert rules
        1.  Find the application group for which you want to disable all alert rules and choose **More** \> **Disable All Alert Rules** in the **Actions** column.
        2.  In the Disable All Alert Rules message, click **Disable**.
    -   Enable all alert rules

        Find the application group for which you want to enable all alert rules and choose **More** \> **Enable All Alert Rules** in the **Actions** column.


## Disable or enable one or more alert rules for an application group

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Application Groups**.

3.  On the **Application grouping** tab of the **Application Groups** page, find the application group for which you want to disable or enable alert rules and click its name or ID.

4.  In the left-side navigation pane, click **Alert Rule**.

5.  On the Alert Rule page, disable or enable one or more alert rules for the application group.

    -   Disable one or more alert rules
        -   Disable one or more threshold-triggered or custom event-triggered alert rules
            1.  On the Threshold Value Alert tab, find the alert rule that you want to disable and click **Disable** in the **Actions** column. Alternatively, select multiple alert rules and click **Disable** below the alert rule list.
            2.  In the Disable Alert Rule message, click **OK**.
        -   Disable one or more system event-triggered alert rules
            1.  Click the **Event Alert** tab.
            2.  On the Event Alert tab, find the system event-triggered alert rule that you want to disable and click **Disable** in the **Actions** column. Alternatively, select multiple system event-triggered alert rules and click **Disable** below the alert rule list.
            3.  In the Disable Alert Rule message, click **OK**.
    -   Enable one or more alert rules
        -   Enable one or more threshold-triggered or custom event-triggered alert rules
            1.  On the Threshold Value Alert tab, find the alert rule that you want to enable and click **Enable** in the **Actions** column. Alternatively, select multiple alert rules and click **Enable** below the alert rule list.
            2.  In the Enable Alert Rule message, click **OK**.
        -   Enable one or more system event-triggered alert rules
            1.  Click the **Event Alert** tab.
            2.  On the Event Alert tab, find the system event-triggered alert rule that you want to enable and click **Enable** in the **Actions** column. Alternatively, select multiple system event-triggered alert rules and click **Enable** below the alert rule list.
            3.  In the Enable Alert Rule message, click **OK**.

