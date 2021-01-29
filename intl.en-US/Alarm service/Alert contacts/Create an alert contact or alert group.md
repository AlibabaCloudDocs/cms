# Create an alert contact or alert group

Cloud Monitor sends alert notifications to alert contacts and alert groups. You must first create an alert contact and an alert group, and then add the alert contact to the alert group. After that, you can specify the alert group to receive alert notifications when you create an alert rule.

## Create an alert contact

You can add an alert contact to multiple alert groups.

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, choose **Alerts** \> **Alert Contacts**.

3.  On the Alert Contacts tab, click **Create Alert Contact**.

4.  In the Set Alert Contact panel,enter the name, email address, and DingTalk chatbot of the alert contact, and retain the default value **Automatic** for the **Alert Notification Information Language** parameter.

    **Note:** **Automatic** indicates that Cloud Monitor automatically selects the language of alert notifications based on the language that you use to create your Alibaba Cloud account.

5.  Verify the parameters and then click **OK**.

6.  Optional. Activate the email address and phone number of the alert contact.

    By default, the email address and phone number of the alert contact are in the **Pending Activation** state. After the alert contact receives an email and text message that contain the activation links, the alert contact must activate the email address and phone number within 24 hours. Otherwise, the alert contact cannot receive alert notifications. After the email address and phone number are activated, they are displayed in the alert contact list.


## Create an alert group

An alert group is a group of one or more alert contacts.

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, choose **Alerts** \> **Alert Contacts**.

3.  Click the **Alert Contact Group** tab.

4.  On the Alert Contact Group tab, click **Create Alert Contact Group**.

5.  In the Create Alert Contact Group panel, specify the alert group name and add alert contacts to the alert group.

6.  Click **Confirm**.


## Add multiple alert contacts to an alert group at a time

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, choose **Alerts** \> **Alert Contacts**.

3.  On the Alert Contacts tab, select multiple alert contacts.

4.  Click **Add to a contact group**.

5.  In the Confirm dialog box, select the alert group.

6.  Click **OK**.


