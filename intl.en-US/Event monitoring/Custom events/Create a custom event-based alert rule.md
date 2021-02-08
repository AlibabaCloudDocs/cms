# Create a custom event-based alert rule

Cloud Monitor manages system events and custom events of Alibaba Cloud services in a centralized manner. You can configure alert rules for events of Alibaba Cloud services. This allows you to receive alert notifications at the earliest opportunity when exceptions occur. Then, you can efficiently analyze and troubleshoot issues. This topic describes how to create a custom event-based alert rule.

The following table describes the event types and Alibaba Cloud services that are supported by Cloud Monitor.

|Event type|Description|Supported Alibaba Cloud services|
|----------|-----------|--------------------------------|
|[System events](#d7e48)|Cloud Monitor provides a centralized platform for you to query system events that are generated for different Alibaba Cloud services. This allows you to track the use of Alibaba Cloud services and receive alert notifications at the earliest opportunity.|[Supported Alibaba Cloud services and system events](/intl.en-US/Appendix 2: System Events/Overview.md)|
|[Custom events](/intl.en-US/Event monitoring/Custom events/Create a custom event-based alert rule.md)|You can call an API operation of Cloud Monitor to report the anomalous events that occur in your Alibaba Cloud services to Cloud Monitor. This allows you to track the use of the Alibaba Cloud services and receive alert notifications at the earliest opportunity.|All Alibaba Cloud services supported by Cloud Monitor|

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Event Monitoring**.

3.  On the Event Monitoring page, click the **Alert Rules** tab.

4.  On the Alert Rules tab, click the **Custom Event** tab.

5.  On the Custom Event tab, click **Create Event Alert**.

6.  In the Create / Modify Event Alert panel, set the parameters of the custom event-triggered alert rule.

    |Parameter|Description|
    |---------|-----------|
    |**Alert Rule Name**|The name of the event-triggered alert rule.|
    |**Application Groups**|Cloud Monitor sends an alert notification only when the specified custom event occurs on a resource in the application group.|
    |**Event Name**|The name of the custom event.|
    |**Rule Description**|The details of the event-triggered alert rule. An alert notification is sent only when the alert is generated for the specified number of times within the specified time period. The time period can be 1, 2, 3, 4, or 5 minutes.|
    |**Notification Method**|The notification method of the event alert. Valid value:Email + DingTalk |
    |**Effective From**|The time period during which the alert rule is effective. Cloud Monitor checks whether monitoring data meets the alert rule only during the effective period. Valid values: 00:00 to 23:59.|
    |**Alert Callback**|Set the callback URL and request method. Enter a callback URL that is reachable over the Internet. Cloud Monitor sends a POST or GET request to push alert information to the specified callback URL. Only HTTP requests are supported. For more information about how to set callback URLs, see [Use the alert callback feature](/intl.en-US/Alarm service/Alarm rules/Use the alert callback feature.md).|

7.  Click **OK**.


## Related operations

On the Custom Event tab, find the custom event-based alert rule that you want to manage and click **View**, **Alert Logs**, **Modify**, **Disable**, **Enable**, or **Delete** in the **Actions** column to perform the corresponding operation for the alert rule.

