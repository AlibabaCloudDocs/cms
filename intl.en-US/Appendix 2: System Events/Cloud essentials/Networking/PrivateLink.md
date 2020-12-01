# PrivateLink

This topic describes the system events for Private Network Connection.

|Type|Event name|Description|State|Level|
|----|----------|-----------|-----|-----|
|Accept|Endpoint:Connection:Accept|The endpoint connection request is accepted.|Executed|Info|
|Reject|Endpoint:Connection:Reject|The endpoint connection request is rejected.|Executed|Info|
|Accept|Endpoint:Connection:Zone:Accept|One or more zones are added to the endpoint connection.|Executed|Info|
|Delete|Endpoint:Connection:Zone:Delete|One or more zones are deleted from the endpoint connection.|Executed|Info|
|Accept|Service:Connection:Auto\_Accept|The endpoint connection requests are automatically accepted.|Executed|Critical|
|Delete|Service:Connection:Delete|The endpoint connection is deleted.|Executed|Info|
|Accept|Service:Connection:Manual\_Accept|The endpoint connection requests are manually accepted.|Executed|Info|
|Reject|Service:Connection:Reject|The endpoint connection is rejected.|Executed|Info|
|Accept|Service:Connection:Zone:Accept|One or more zones are added to the endpoint service.|Executed|Info|
|Delete|Service:Connection:Zone:Delete|One or more zones are deleted from the endpoint service.|Executed|Info|

