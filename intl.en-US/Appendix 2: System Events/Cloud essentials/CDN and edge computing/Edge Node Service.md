# Edge Node Service

This topic describes the system events for Edge Node Service \(ENS\).

|Type|Event|Description|State|Level|
|----|-----|-----------|-----|-----|
|Exception|Disk:Stalled:Executed|The impact on the disk performance ends.|Executed|Critical|
|Exception|Disk:Stalled:Executing|The impact on the disk performance starts.|Executing|Critical|
|Notice|EnsInstance:Create:Executed|The instance is created.|Executed|Critical|
|Notice|EnsInstance:Delete:Executed|The instance is deleted.|Executed|Critical|
|Exception|EnsRegion:NetworkDown:Executed|The network of the edge node is recovered.|Executed|Critical|
|Exception|EnsRegion:NetworkDown:Executing|The edge node is disconnected over the network.|Executing|Critical|
|Maintenance|EnsRegion:NetworkMigration:Canceled|The network cutover is canceled for the edge node.|Canceled|Info|
|Maintenance|EnsRegion:NetworkMigration:Executed|The network cutover is completed for the edge node.|Executed|Info|
|Maintenance|EnsRegion:NetworkMigration:Executing|The network cutover starts for the edge node.|Executing|Critical|
|Maintenance|EnsRegion:NetworkMigration:Scheduled|The network cutover is scheduled for the edge node.|Scheduled|Warn|
|Exception|EnsRegion:PortError:Executed|The port of the edge node is recovered.|Executed|Critical|
|Exception|EnsRegion:PortError:Executing|An error occurs on the port of the edge node.|Executing|Critical|
|Exception|Instance:SystemFailure.Reboot:Executed|The instance reboot due to a system error is complete.|Executed|Critical|
|Exception|Instance:SystemFailure.Reboot:Executing|The instance reboot due to a system error starts.|Executing|Critical|
|Status Notification|AUTOSCALING:SCALE\_IN\_ERROR|The scale-in activity of the scaling group fails.|unNormal|Critical|
|Status Notification|AUTOSCALING:SCALE\_IN\_START|The scale-in activity of the scaling group starts.|Normal|Info|
|Status Notification|AUTOSCALING:SCALE\_IN\_SUCCESS|The scale-in activity of the scaling group is successful.|Normal|Info|
|Status Notification|AUTOSCALING:SCALE\_OUT\_ERROR|The scale-out activity of the scaling group fails.|unNormal|Critical|
|Status Notification|AUTOSCALING:SCALE\_OUT\_START|The scale-out activity of the scaling group starts.|Normal|Info|
|Status Notification|AUTOSCALING:SCALE\_OUT\_SUCCESS|The scale-out activity of the scaling group is successful.|Normal|Info|
|Status Notification|AUTOSCALING:SCALE\_REJECT|The scaling activity of the scaling group is rejected.|Warn|Warn|
|Maintenance|AUTOSCALING:SCHEDULE\_TASK\_EXPIRING|The scheduled task expires.|Warn|Warn|

