# Create an alert template

You can save alert rules for metrics of various cloud services as a template. If you have a large amount of resources to monitor, alert templates can save you a lot of effects in defining alert rules. When you create or modify alert rules, you can apply alert templates without defining each alert rule from scratch.

-   Alert templates must be used together with application groups. You can create an application group, and then create and apply an alert template to the application group to create alert rules for the application group. This simplifies the creation and maintenance of alert rules. For more information about how to create an application group, see [Create an application group](/intl.en-US/Application groups/Create an application group.md).
-   You must obey the following limits when you create an alert template:
    -   You can create up to 100 alert templates for each Alibaba Cloud account.
    -   Each alert template can contain up to 30 metrics.

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, choose **Alerts** \> **Alert Templates**.

3.  On the Alert Templates page, click **Create Alert Template** in the upper-right corner.

4.  In the Create/modify alert templates pane, enter the template name and set alert rules for cloud services as required.

    You can also use the template clone feature to create an alert template. Select the template to be cloned and set alert rules for cloud services as required.

5.  Click **OK**.

6.  In the Create/modify alert template complete message, click **OK**.

    **Note:** If you click **Cancel**, the alert template is created but not applied to application groups. You can apply the alert template to application groups later. For more information, see [Apply an alert template to an application group](/intl.en-US/Application groups/Apply an alert template to an application group.md).

7.  In the Apply Template to Group dialog box, select application groups and set the Muted, Effective Period, HTTP CallBack, and Option parameters.

8.  Click **OK**.

9.  In the Apply Template to Group message, click **OK**.


