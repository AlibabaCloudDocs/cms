# System event-triggered alerts

Cloud Monitor manages system events and custom events of Alibaba Cloud services in a centralized manner. You can configure alert rules for system events of Alibaba Cloud services. This allows you to receive alert notifications at the earliest opportunity when exceptions occur. Then, you can efficiently analyze and troubleshoot issues. This topic shows you how to create an event-triggered alert rule and test a system event-triggered alert rule.

The following table describes the event types and Alibaba Cloud services that are supported by Cloud Monitor.

|Event type|Description|Supported Alibaba Cloud services|
|----------|-----------|--------------------------------|
|System events|Cloud Monitor provides a centralized platform for you to query system events that are generated for different Alibaba Cloud services. This allows you to track the use of Alibaba Cloud services and receive alert notifications at the earliest opportunity.|[Supported Alibaba Cloud services and system events](/intl.en-US/Appendix 2: System Events/Overview.md)|
|Custom events|You can call an API operation of Cloud Monitor to report the anomalous events that occur in your Alibaba Cloud services to Cloud Monitor. This allows you to track the use of the Alibaba Cloud services and receive alert notifications at the earliest opportunity.|All Alibaba Cloud services supported by Cloud Monitor|

## Create a system event-triggered alert rule

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Event Monitoring**.

3.  On the Event Monitoring page, click the **Alert Rules** tab.

4.  On the Alert Rules tab, click the **System Event** tab and then **Create Event Alert**.

5.  In the Create / Modify Event Alert panel, set the parameters of the system event-triggered alert rule.

    |Parameter|Description|
    |---------|-----------|
    |**Alert Rule Name**|The name of the event-triggered alert rule.|
    |**Product Type**|The Alibaba Cloud service to which the event-triggered alert rule is applied. For more information about the Alibaba Cloud services supported by Cloud Monitor, see [Overview](/intl.en-US/Appendix 2: System Events/Overview.md).|
    |**Event Type**|The type of the event that triggers alerts. For more information about the types of the events supported by each Alibaba Cloud service, see [Overview](/intl.en-US/Appendix 2: System Events/Overview.md).|
    |**Event Level**|The level of the event that triggers alerts. For more information about the levels of the events supported by each Alibaba Cloud service, see [Overview](/intl.en-US/Appendix 2: System Events/Overview.md).|
    |**Event Name**|The name of the event that triggers alerts. For more information about the names of the events supported by each Alibaba Cloud service, see [Overview](/intl.en-US/Appendix 2: System Events/Overview.md).|
    |**Resource Range**|The range of the resources to which the event-triggered alert rule is applied. Valid values:    -   **All Resources**: If the **Resource Range** parameter is set to **All Resources**, Cloud Monitor sends an alert notification when the specified event occurs on a resource.
    -   **Application Groups**: If the **Resource Range** parameter is set to **Application Groups**, Cloud Monitor sends an alert notification only when the specified event occurs on a resource in the application group. |
    |**Contact Group**|The alert group that receives alert notifications.|
    |**Notification Method**|The level and notification method of the event alert. Valid value:Info \(Email ID+DingTalk Robot\) |
    |**Function service**|The specific function of Function Compute to which the event alert is delivered.|
    |**MNS queue**|The specified queue in Message Service \(MNS\) to which the event alert is delivered.|
    |**Log Service**|The specified Logstore in Log Service to which the event alert is delivered.|
    |**URL callback**|Set the callback URL and request method. Enter a callback URL that is reachable over the Internet. Cloud Monitor sends a POST or GET request to push alert information to the specified callback URL. Only HTTP requests are supported. For more information about how to set callback URLs, see [Use the alert callback feature](/intl.en-US/Alarm service/Alarm rules/Use the alert callback feature.md).|

6.  Click **OK**.


## Test a system event-triggered alert rule

**Note:** You can test only a system event-triggered alert rule that is associated with a specific Alibaba Cloud service and a specific event.

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Event Monitoring**.

3.  On the Event Monitoring page, click the **Alert Rules** tab.

4.  On the Alert Rules tab, click the **System Event** tab. Then, find the alert rule that you want to test and click **test** in the **Actions** column.

5.  In the Create event test panel, select the event to be tested.

6.  In the **Content\(JSON\)** section, modify the event content such as the instance ID as needed.

7.  Click **OK**.

    Cloud Monitor generates an event based on the event content to trigger the alert rule.


## Related operations

On the System Event tab, find the alert rule that you want to manage and click **Modify**, **Disable**, **Enable**, or **Delete** in the **Actions** column to perform the corresponding operation for the alert rule.

