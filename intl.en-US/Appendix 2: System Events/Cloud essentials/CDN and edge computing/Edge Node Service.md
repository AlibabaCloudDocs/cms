# Edge Node Service

This topic describes the system events of Edge Node Service \(ENS\).

|Type|Event|Description|State|Level|
|----|-----|-----------|-----|-----|
|Exception|Disk:Stalled:Executed|The impact on the disk performance ends.|Executed|Critical|
|Exception|Disk:Stalled:Executing|The impact on the disk performance starts.|Executing|Critical|
|Notice|EnsInstance:Create:Executed|The instance is created.|Executed|Critical|
|Notice|EnsInstance:Delete:Executed|The instance is deleted.|Executed|Critical|
|Exception|EnsRegion:NetworkDown:Executed|The network of the edge node is recovered.|Executed|Critical|
|Exception|EnsRegion:NetworkDown:Executing|The edge node is disconnected from the network.|Executing|Critical|
|Maintenance|EnsRegion:NetworkMigration:Canceled|The network cutover is canceled for the edge node.|Canceled|Info|
|Maintenance|EnsRegion:NetworkMigration:Executed|The network cutover is completed for the edge node.|Executed|Info|
|Maintenance|EnsRegion:NetworkMigration:Executing|The network cutover is started for the edge node.|Executing|Critical|
|Maintenance|EnsRegion:NetworkMigration:Scheduled|The network cutover is scheduled for the edge node.|Scheduled|Warn|
|Executed|EnsRegion:NetworkWaterLevel:Executed|The bandwidth usage of the edge node is restored.|Executed|Warn|
|Executing|EnsRegion:NetworkWaterLevel:Executing|An exception occurs in the bandwidth usage of the edge node.|Executing|Warn|
|Exception|EnsRegion:PortError:Executed|The port of the edge node recovers.|Executed|Critical|
|Exception|EnsRegion:PortError:Executing|An exception occurs on the port of the edge node.|Executing|Critical|
|Exception|Instance:SystemFailure.Reboot:Executed|The instance reboot that is caused by a system error is completed.|Executed|Critical|
|Exception|Instance:SystemFailure.Reboot:Executing|The instance reboot that is caused by a system error starts.|Executing|Critical|

