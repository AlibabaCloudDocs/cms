# Receive alert notifications in a DingTalk group

This topic shows you how to receive alert notifications in a DingTalk group.

An alert contact is created. For more information, see [Create an alert contact or alert group](/intl.en-US/Alarm service/Alert contacts/Create an alert contact or alert group.md).

After you add the webhook URL of a DingTalk chatbot to an existing alert contact, you can receive alert notifications by using the DingTalk group.

## Step 1: Create a DingTalk chatbot on DingTalk for PC

1.  Start DingTalk for PC and go to the DingTalk group in which you want to receive alert notifications.

2.  Click **Group Settings** in the upper-right corner.

3.  In the Group Settings panel, click **Group Assistant**.

4.  In the Group Assistant panel, click **Add Robot**.

5.  In the **Please choose which robot to add** section of the ChatBot dialog box, click **Custom**.

6.  In the Robot details dialog box, click **Add**.

7.  In the Add Robot dialog box, configure the chatbot information.

    -   Enter a chatbot name, such as Cloud Monitor alert notifications.
    -   Select **Custom Keywords** and add keywords, such as Alibaba Cloud, Service, Cloud Monitor, Monitor, and ECS, one by one.
8.  Select **I have read and accepted <<DingTalk Custom Robot Service Terms of Service\>\>** and click **Finished**.

9.  Click **Copy** to copy the webhook URL.


## Step 2: Add the webhook URL of the DingTalk chatbot to an alert contact

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, choose **Alerts** \> **Alert Contacts**.

3.  On the Alert Contacts tab, find the alert contact that you want to modify and click **Edit** in the **Actions** column.

4.  In the Set Alert Contact panel, enter the webhook URL of the DingTalk chatbot.

5.  Verify the parameters and then click **OK**.


