# SAG

This topic describes the system events for Smart Access Gateway \(SAG\).

|Event|Description|Type|State|Level|
|-----|-----------|----|-----|-----|
|AccessGatewayFailover|The access point fails over.|Maintenance|Agwfailover|Info|
|ConnectionDisconnect|The network is disconnected.|Exception|Disconnect|Critical|
|DeviceHacked|The device is under attack.|Exception|Hacked|Critical|
|DeviceLinkDown|An error occurs in the link of the device.|Exception|Linkdown|Critical|
|DeviceOffline|The device is offline.|Status Notification|Offline|Critical|
|DeviceOnline|The device is online.|Status Notification|Online|Info|
|DeviceSwitched|A switchover occurs between the active and standby devices.|Maintenance|Switched|Critical|
|DeviceWanLinkDown|An error occurs in the wide area network \(WAN\) link of the device.|Exception|WanLinkDown|Critical|
|DeviceWanLinkSwitched|A switchover occurs between the active and standby WAN links.|Maintenance|WanLinkSwitched|Critical|
|DeviceWanLinkUp|The WAN link of the device is recovered.|Exception|WanLinkUp|Info|

