# Status codes

If an error occurs when you use the availability monitoring feature of Cloud Monitor to detect the availability of a specified path or port, the corresponding status code is returned.

The following table lists the status codes.

|Protocol|Status code|Description|
|:-------|:----------|:----------|
|HTTP|610|The status code returned because the connection times out. If Cloud Monitor does not receive a response within 5 seconds after Cloud Monitor sends an HTTP request, Cloud Monitor determines that the connection times out.|
|611|The status code returned because the monitoring fails.|
|Telnet|630|The status code returned because the connection times out. If Cloud Monitor does not receive a response within 5 seconds after Cloud Monitor sends a Telnet request, Cloud Monitor determines that the connection times out.|
|631|The status code returned because the monitoring fails.|

