# How has event monitoring been updated?

This topic describes the update to the event monitoring feature of Cloud Monitor.

## Feature update

The event monitoring feature is updated to allow you to configure event-triggered alert rules. Before the update, you can configure event-triggered alert rules only on the Alert Rules page. After the update, you can query events and configure event-triggered alert rules in the same place.

## Update details

1.  The Event Monitoring page provides the Alert Rules tab for you to manage event-triggered alert rules. You can no longer configure alert rules for the following events in alert templates: no heartbeat of the Cloud Monitor agent, failover or faults of ApsaraDB RDS, ApsaraDB for Redis, or ApsaraDB for Memcache instances, status or node exceptions of ApsaraDB for MongoDB or Container Service instances, and synchronization exceptions in disaster recovery for ApsaraDB RDS and ApsaraDB for Redis instances.
2.  You can subscribe to events when you create an application group. After you enable event subscription for an application group, you can receive notifications for critical and warning events that occur on the resources in the application group.
3.  After the update, you can still use existing event-triggered alert rules. However, you cannot modify these rules. If the existing rules cannot meet your requirements, you can create event-triggered alert rules on the Event Monitoring page and use the new rules to replace the existing rules.

The update does not affect your online services and existing alert configurations.

For more information about the event monitoring feature of Cloud Monitor, see [Cloud product system event monitoring](/intl.en-US/Event monitoring/Cloud product events/View system events.md) and [Use the system event alert feature](/intl.en-US/Event monitoring/Cloud product events/Use the system event alert feature.md).

