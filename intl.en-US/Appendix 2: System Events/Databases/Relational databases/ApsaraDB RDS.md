# ApsaraDB RDS

This topic describes the system events for ApsaraDB RDS.

|Type|Event|Description|Status|Level|
|----|-----|-----------|------|-----|
|Maintenance|Instance\_Failover|An instance failover occurs.|Executed|Warn|
|Exception|Instance\_Failure\_End|An instance failure ends.|Executed|Critical|
|Exception|Instance\_Failure\_Start|An instance failure starts.|Executing|Critical|
|Maintenance|Instance:SystemMaintenance.Transfer:Scheduled|The instance migration is scheduled.|Scheduled|Warn|
|Maintenance|Instance:SystemMaintenance.Transfer:Executing|The instance is being migrated.|Executing|Warn|
|Maintenance|Instance:SystemMaintenance.Transfer:Executed|The instance is migrated.|Executed|Warn|
|Maintenance|Instance:SystemMaintenance.Transfer:Canceled|The instance migration is canceled.|Canceled|Warn|
|Maintenance|Instance:SystemMaintenance.MinorVersionUpgrade:Scheduled|The instance update to a minor version is scheduled.|Scheduled|Warn|
|Maintenance|Instance:SystemMaintenance.MinorVersionUpgrade:Executing|The instance is being updated to a minor version.|Executing|Warn|
|Maintenance|Instance:SystemMaintenance.MinorVersionUpgrade:Executed|The instance is updated to a minor version.|Executed|Warn|
|Maintenance|Instance:SystemMaintenance.MinorVersionUpgrade:Canceled|The instance update to a minor version is canceled.|Canceled|Warn|

