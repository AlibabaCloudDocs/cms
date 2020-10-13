# DBS

This topic describes the system events for Database Backup.

|Type|Event|Description|Status|Level|
|----|-----|-----------|------|-----|
|StatusNotification|CloseContBackup|Incremental backup is disabled.|Failed|Info|
|Exception|ContBackupFail|An exception occurs during incremental backup.|Failed|Warn|
|StatusNotification|DataRestoreFail|An exception occurs during data recovery.|Failed|Warn|
|StatusNotification|DataRestoreSuccess|Data recovery is successful.|Running|Warn|
|Exception|FullBackupFail|An error occurs during full backup.|Failed|Warn|
|StatusNotification|InstancePause|The backup plan is suspended.|Failed|Info|
|StatusNotification|InstanceStart|The backup plan starts.|Running|Info|
|StatusNotification|OpenContBackup|Incremental backup is enabled.|Running|Info|

