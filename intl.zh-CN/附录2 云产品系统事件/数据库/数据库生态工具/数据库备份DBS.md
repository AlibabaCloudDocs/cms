# 数据库备份DBS

通过本文您可以了解数据库备份DBS的系统事件。

|事件类型|事件名称|事件含义|事件状态|事件等级|
|----|----|----|----|----|
|StatusNotification|CloseContBackup|关闭增量日志备份|Failed|Info|
|Exception|ContBackupFail|增量备份异常|Failed|Warn|
|StatusNotification|DataRestoreFail|数据恢复异常|Failed|Warn|
|StatusNotification|DataRestoreSuccess|数据恢复成功|Running|Warn|
|Exception|FullBackupFail|全量备份异常|Failed|Warn|
|StatusNotification|InstancePause|备份计划暂停|Failed|Info|
|StatusNotification|InstanceStart|备份计划启动|Running|Info|
|StatusNotification|OpenContBackup|开启增量日志备份|Running|Info|

