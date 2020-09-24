# Apply an alert template to an application group

If you have a large amount of resources, we recommend that you add these resources to application groups based on business needs. Then, you can create and apply alert templates to the application groups, which simplifies the creation and maintenance of alert rules. Alert templates must be used together with application groups. You can apply alert templates to application groups to create alert rules for resources from different services.

-   An application group is created. For more information, see [Create an application group](/intl.en-US/Application groups/Create an application group.md).
-   An alert template is created. For more information, see [Create an alert template](/intl.en-US/Alarm service/Alert templates/Use alarm templates.md).

When an alert template is applied to an application group, Cloud Monitor automatically deletes the original alert rules configured for the application group and creates alert rules based on the alert template.

## Apply an alert template to an application group on the Application Groups page

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Application Groups**.

3.  On the **Application grouping** tab of the **Application Groups** page, click the name or ID of the application group to which you want to apply an alert template.

4.  On the Group Resource page, click **Apply Template to Group** in the upper-right corner.

5.  In the Apply Template to Group dialog box, select an alert template and set the Muted, Effective From, HTTP CallBack, and Option parameters.

6.  Click **OK**.

7.  In the Apply Template to Group message, click **OK**.


## Apply an alert template to an application group on the Alerts page

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, choose **Alerts** \> **Alert Templates**.

3.  On the Alert Templates page, find the alert template that you want to apply to the application group and click **Apply to Group** in the **Actions** column.

4.  In the Apply Template to Group dialog box, select an alert template and set the Muted, Effective From, HTTP CallBack, and Option parameters.

5.  Click **OK**.

6.  In the Apply Template to Group message, click **OK**.


