# Status codes

The availability monitoring feature of Cloud Monitor returns a status code when an exception occurs during the monitoring. The following table describes the status codes that may be returned by the availability monitoring feature.

|Protocol|Status code|Description|
|:-------|:----------|:----------|
|HTTP|610|The status code returned because the connection times out. If Cloud Monitor does not receive a response within 5 seconds after Cloud Monitor sends an HTTP request, Cloud Monitor determines that the connection times out.|
|HTTP|611|The status code returned because the monitoring fails.|
|Telnet|630|The status code returned because the connection times out. If Cloud Monitor does not receive a response within 5 seconds after Cloud Monitor sends a Telnet request, Cloud Monitor determines that the connection times out.|
|Telnet|631|The status code returned because the monitoring fails.|

