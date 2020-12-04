# Status codes

The following tables list the status codes of each protocol generated in site monitoring of Cloud Monitor and the common HTTP status codes.

## Custom status codes of Cloud Monitor

|Protocol|Status code|Description|
|:-------|:----------|:----------|
|HTTP|610|The error code returned because the connection or the Secure Sockets Layer \(SSL\) certificate exchange has timed out. The timeout period is 30 seconds.|
|613|The error code returned because an error has occurred in DNS resolution.|
|615|The error code returned because expected content is not found in the response or unexpected content is found in the response.|
|616|The error code returned because the authentication has failed.|
|611|The error code returned because the monitoring has failed due to other causes.|
|617|The error code returned because the maximum number of redirections has been exceeded.

-   The detection points provided by Alibaba Cloud support a maximum of five redirections with the status codes 3XX.
-   The detection points provided by carriers support a maximum of two redirections with the status codes 3XX. |
|703|The error code returned because the server cannot be monitored over the internal network. For more information about how to monitor servers over the internal network, see [Create a site monitoring task](/intl.en-US/Site Monitoring/Create a site monitoring task.md).|
|PING|550|The error code returned because the network connection has failed.|
|610|The error code returned because no response has been returned within 2 seconds for any of the sent packets.|
|613|The error code returned because the hostname cannot be resolved to an IP address.|
|703|The error code returned because the server cannot be monitored over the internal network. For more information about how to monitor servers over the internal network, see [Create a site monitoring task](/intl.en-US/Site Monitoring/Create a site monitoring task.md).|
|TCP|550|The error code returned because the socket cannot be opened. This error occurs if system resources have been completely consumed.|
|610|The error code returned because no response has been returned or the response has timed out.|
|611|The error code returned because the connection has timed out or is rejected.|
|615|The error code returned because expected content is not found in the response or unexpected content is found in the response.|
|703|The error code returned because the server cannot be monitored over the internal network. For more information about how to monitor servers over the internal network, see [Create a site monitoring task](/intl.en-US/Site Monitoring/Create a site monitoring task.md).|
|UDP|550|The error code returned because the socket cannot be opened. This error occurs if system resources have been completely consumed.|
|611|The error code returned because the hostname cannot be resolved and the connection has failed.|
|610|The error code returned because the request cannot be sent or the response failed to be received.|
|615|The error code returned because expected content is not found in the response or unexpected content is found in the response.|
|703|The error code returned because the server cannot be monitored over the internal network. For more information about how to monitor servers over the internal network, see [Create a site monitoring task](/intl.en-US/Site Monitoring/Create a site monitoring task.md).|
|DNS|610|The error code returned because an error has occurred in DNS resolution.|
|613|The error code returned because the DNS query has failed.|
|615|The error code returned because expected content is not found in the response or unexpected content is found in the response.|
|703|The error code returned because the server cannot be monitored over the internal network. For more information about how to monitor servers over the internal network, see [Create a site monitoring task](/intl.en-US/Site Monitoring/Create a site monitoring task.md).|
|SMTP|610|The error code returned because the connection has timed out.|
|611|The error code returned because the site cannot be accessed due to failed DNS resolution, invalid email address, or failed SMTP client initialization.|
|616|The error code returned because the logon request is rejected.|
|703|The error code returned because the server cannot be monitored over the internal network. For more information about how to monitor servers over the internal network, see [Create a site monitoring task](/intl.en-US/Site Monitoring/Create a site monitoring task.md).|
|POP3|611|The error code returned because the site cannot be accessed.|
|703|The error code returned because the server cannot be monitored over the internal network. For more information about how to monitor servers over the internal network, see [Create a site monitoring task](/intl.en-US/Site Monitoring/Create a site monitoring task.md).|
|FTP|610|The error code returned because the FTP transmission has failed.|
|611|The error code returned because the site cannot be accessed due to failed DNS resolution, invalid email address, or failed SMTP client initialization.|
|616|The error code returned because the logon failed.|
|703|The error code returned because the server cannot be monitored over the internal network. For more information about how to monitor servers over the internal network, see [Create a site monitoring task](/intl.en-US/Site Monitoring/Create a site monitoring task.md).|

## Common HTTP status codes

|Status code|Status message|Description|
|:----------|:-------------|:----------|
|200|OK|The status code returned because the request is successful. All status codes 2XX indicate successful requests.|
|300|Multiple Choices|The status code returned because the server can perform multiple operations based on the request. The server selects one operation to perform based on the user agent or provides a list of operations for the user agent to choose.|
|301|Moved Permanently|The status code returned because the requested web page is permanently moved to a new URL. If the server returns this status code in response to a GET or HEAD request, the server redirects the request to the new URL. You can use this status code to notify Googlebot that a web page or a website is permanently moved to a new URL.|
|302|Found|The status code returned because the requested web page is temporarily moved to another URL. The user agent must continue to use the original URL for future requests. The server redirects the request to the new URL. This is similar to the operation performed by the server when the status code 301 is returned in response to a GET or HEAD request.|
|303|See Other|The status code returned because the user agent must send a GET request to another URL. The server redirects all requests other than the HEAD request to the new URL.|
|304|Not Modified|The status code returned because the requested web page has not been modified since the last request. If the server returns this status code, the content of the web page is not returned in the response.|
|305|Use Proxy|The status code returned because the requested resource must be accessed by using the proxy. If the server returns the status code, the server specifies the proxy in the response.|
|400|Bad Request|The status code returned because the server cannot process the request due to the invalid request syntax.|
|401|Unauthorized|The status code returned because the user agent must pass the authentication. The server may return this status code after the logon.|
|403|Forbidden|The status code returned because the server rejected the request.|
|404|Not Found|The status code returned because the server cannot find the requested web page. For example, the server returns this status code if the requested web page does not exist on the server.|
|405|Method Not Allowed|The status code returned because the request method is not supported.|
|406|Not Acceptable|The status code returned because the content of the request is not acceptable.|
|407|Proxy Authentication Required|The status code returned because the user agent is required to use the proxy to pass the authentication. The status code 407 is similar to the status code 401. If the server returns the status code, the server specifies the proxy in the response.|
|408|Request Timeout|The status code returned because the server timed out waiting for the request.|
|409|Conflict|The status code returned because the request cannot be completed due to a conflict. The server returns the information about the conflict in the response. Conflicts may occur in response to a PUT request that conflicts with an earlier request. In this case, the server returns this status code and the differences between the two requests.|
|411|Length Required|The status code returned because the server has refused to accept the request that does not specify the length of the content.|
|412|Precondition Failed|The status code returned because the server cannot meet one of the prerequisites set by the user agent in the request.|
|413|Request Entity Too Large|The status code returned because the size of the request has exceeded the processing capacity of the server.|
|414|Request-URI Too Long|The status code returned because the URI provided is too long for the server to process.|
|415|Unsupported Media Type|The status code returned because the request entity has a media type that the server does not support.|
|416|Requested Range Not Satisfiable|The status code returned because the range of the requested web page is invalid.|
|417|Expectation Failed|The status code returned because the server cannot meet the requirements of the Expect request header field.|
|499|Client Closed Request|The status code returned because the client closed the request before the server could send a response.|
|500|Internal Server Error|The status code returned because the request cannot be completed due to an internal server error.|
|501|Not Implemented|The status code returned because the server does not support the feature required to complete the request. For example, the server returns this status code when the server cannot recognize the request method.|
|502|Bad Gateway|The status code returned because the server that acts as a gateway or proxy has received an invalid response from the upstream server.|
|503|Service Unavailable|The status code returned because the server is temporally unable to handle the request due to a temporary overloading or maintenance of the server.|
|504|Gateway Timeout|The status code returned because the server that acts as a gateway or proxy does not receive a response from the upstream server within the timeout period.|
|505|HTTP Version Not Supported|The status code returned because the server does not support the HTTP protocol version that is used in the request.|

