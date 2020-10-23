# Create a custom event-based alert rule

This topic describes how to create a custom event-based alert rule. Custom event-based alert rules allow you to receive alert notifications immediately after the specified custom events occur.

When Cloud Monitor receives custom events that are specified in custom event-based alert rules, Cloud Monitor sends alert notifications by using one of the following methods:

-   Sends alert notifications to the specified email address or DingTalk group.
-   Pushes alerts to the specified callback URL. This allows you to automate the handling process based on your scenario.

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Event Monitoring**.

3.  On the Event Monitoring page, click the **Alert Rules** tab.

4.  On the Alert Rules tab, click **Create Event Alert**.

5.  In the Create / Modify Event Alert panel, set the parameters.

    |Parameter|Description|
    |---------|-----------|
    |**Alert Rule Name**|The name of the alert rule.|
    |**Event Type**|The type of the event. Valid values:     -   **System Event**
    -   **Custom Event**
Select **Custom Event**. |
    |**Application Groups**|The application group to which the alert rule applies. An alert notification is sent only when the specified custom event occurs on resources in the application group.|
    |**Event Name**|The name of the event for which an alert notification is sent.|
    |**Rule Description**|The rule for sending an alert notification. An alert notification is sent only when the event occurs for the specified number of times within the specified time period. The time period can be 1, 2, 3, 4, or 5 minutes.|
    |**Notification Method**|The methods of sending an alert notification. Value:Email + DingTalk |
    |**Effective From**|The time period during which the alert rule is effective. Cloud Monitor checks whether monitoring data meets the alert rule only within the effective period.|
    |**Alert Callback**|The callback URL that can be accessed over the Internet. Cloud Monitor sends a POST request to push an alert to the specified callback URL. Only HTTP requests are supported. For more information, see [Use alert callbacks](/intl.en-US/Alarm service/Alarm rules/Use alert callbacks.md).|

6.  Click **OK**.


