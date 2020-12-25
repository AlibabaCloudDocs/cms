# Create a site monitoring task

You can create a site monitoring task to monitor sites on the Internet and analyze network quality or performance.

-   Alert contacts and alert groups are created if you need to configure alert rules for a site monitoring task. When you configure an alert rule, you can select an alert group as the alert notification recipient. For more information, see [Create an alert contact or alert group](/intl.en-US/Alarm service/Alert contacts/Create an alert contact or alert group.md).
-   A callback URL that can be accessed over the Internet is prepared if you need to enable the alert callback feature for alert rules. In addition, URL callback is enabled as an alert notification method in your existing O&M or notification system.

Site monitoring sends detection requests that simulate real user access from Alibaba Cloud data centers to your site to test and monitor access to your site. Site monitoring is applicable to the following scenarios:

-   Create a site monitoring task to obtain the information about the destination site, such as the time consumed to resolve the domain name to an IP address, establish the connection, receive the first packet, and download data. The information can help you analyze the performance bottlenecks of your service.
-   Monitor the sites of Alibaba Cloud and carriers at the same time by using the selected detection points. Based on the monitoring results, you can compare the quality of Alibaba Cloud services with that of the services provided by the carriers.
-   Send detection requests from all Alibaba Cloud regions.

## Procedure

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, choose **New Site Monitor** \> **Site Manage**.

3.  On the Site Monitoring page, click **New Monitoring Task**.

4.  Configure the basic information.

    |Parameter|Description|
    |---------|-----------|
    |**Monitor Type**|The monitoring protocol. Valid values: HTTP\(s\), PING, TCP, UDP, DNS, SMTP, POP3, and FTP.|
    |**IP Probe Type**|The IP address type of the detection point. Valid values: IPv4 and IPv6.|
    |**Task Name**|The name of the monitoring task. The value must be 4 to 100 characters in length. It can contain letters, digits, and underscores \(\_\).|
    |**Monitor Address**|The address of the site to be monitored. You can specify multiple addresses at a time. Each address occupies a line. After you save the configurations, Cloud Monitor generates a site monitoring task for each specified site address.|
    |**Monitoring frequency**|The interval at which detection requests are sent. Valid values: 1 min, 5 minutes, 15 minutes, 30 minutes, and 60 minutes. For example, if you select 1 min, a detection point in a region sends a detection request to the monitored site every minute.|
    |**Advanced Settings**|The advanced settings for the selected protocol. For more information, see [Description](#section_08r_0oc_dac).|

5.  Select detection points.

    **Probe points advanced options**: allows you to customize detection points by specifying the carrier and region.

6.  Configure an alert rule.

    |Parameter|Description|
    |---------|-----------|
    |**Availability**|The availability of detection points. Valid values:    -   Number of probe points available

The value is the number of detection results in which the status code is smaller than 400 within a monitoring period.

    -   Available probe point ratio

The value is the percentage of detection results in which the status code is smaller than 400 to all detection results within a monitoring period.

    -   Any Status Code \(Independent Alert\)
    -   All Status Code \(Combined Alert\) |
    |**Average response time**|The average response time of all detection points within a monitoring period.|
    |**Triggered when threshold is exceeded for**|The number of consecutive times that the threshold is exceeded before an alert is triggered. This parameter is used to prevent false alerts caused by occasional network jitters.|
    |**Contact Group**|The object to which alert notifications are sent.|
    |**Notification Methods**|The methods that are used to send alert notifications.|
    |**Channel Silence Time**|The interval of re-sending the notification for an alert before the alert is cleared.|
    |**Effective Time**|The time period during which the alert rule is effective. Cloud Monitor sends alert notifications only within the effective period. Cloud Monitor only records alerts if the alerts are generated in other time periods.|
    |**Alert Callback**|The callback URL that can be accessed over the Internet. Cloud Monitor sends a POST request to push an alert message to the specified callback URL. Only HTTP requests are supported.|

7.  Click **Create**.


## Description

The following tables describe the advanced settings for different protocols.

-   HTTP or HTTPS

    |Parameter|Setting method|Required|Description|
    |---------|--------------|--------|-----------|
    |Monitor Address|URL|Yes|    -   If the HTTPS protocol is used, the URL must contain the https scheme. Example: `https://aliyun.com`.
    -   If you enter a URL that does not have a scheme, the default scheme http is added to the URL. |
    |Request content|Form data or JSON objects|No|If the data is in the JSON format, you must enclose JSON objects in braces \{\}. Otherwise, the data is parsed as form data.|
    |Request method|Radio button|Yes|The HTTP request method. Valid values:

    -   GET
    -   POST
    -   HEAD
Default value: GET. |
    |Match response method|Radio button|Yes|If you specify the response content to match, site monitoring checks whether the first 64 KB of the response body contains the response content to match. The following results may be obtained:

    -   Contains the response content to match.
    -   Does not contain the response content to match.
Site monitoring determines whether to generate an alert based on the mode in which the response is matched.

The detection points of Alibaba Cloud support both Chinese and English. We recommend that you specify the response content to match in English. |
    |Match response content|Text|No|
    |HTTP request header|Multiple lines of text|No|Each HTTP header occupies a line. It is a key-value pair in which the key and value are separated with a colon \(:\). Site monitoring adds the following preset headers to the request:

    -   `Host:${Domain name in the monitored address}`
    -   `Pragma:no-cache`
    -   `Cache-Control:no-cache`
    -   `User-Agent:Chrome/57`
    -   `Accept: */*`
If the request body is a form, the request also contains the following header:

`Content-Type: application/x-www-form-urlencoded;charset=UTF-8`

If your request contains one or more of the preceding headers, the headers are overwritten by your settings.

**Note:** Based on the HTTP protocol, site monitoring converts the keys that you specify in the request headers to the canonical format of MIME header based on the following rules:

    -   The first letter and the letter following a hyphen \(-\) are converted to uppercase letters. For example, accept-encoding is converted to Accept-Encoding.
    -   If a key contains a space or invalid characters, the key remains unchanged. |
    |Cookie|Cookie text|No|The HTTP cookie.|
    |HTTP Authentication Username|Username|No|The username and password used for basic HTTP authentication.|
    |HTTP Authentication Password|Password|No|
    |Certificate verification|Select|No|Specifies whether server name indication \(SNI\) is supported. By default, the check box is cleared, which indicates that SNI is not supported.|
    |Unfollow Redirect|Select|No|Specifies whether to follow redirects if the status code 301 or 302 is returned. By default, the check box is cleared, indicating that redirects are followed.|

-   PING

    |Parameter|Setting method|Required|Description|
    |---------|--------------|--------|-----------|
    |Monitor Address|Domain name or IP address|Yes|N/A|
    |Number of ping packets|Positive integer|Yes|The number of times that the site is pinged. Default value: 20. Valid values: 1 to 40.|

-   TCP or UDP

    |Parameter|Setting method|Required|Description|
    |---------|--------------|--------|-----------|
    |Monitor Address|Domain name or IP address|Yes|-|
    |Request content format|Radio button|Yes|This parameter takes effect only when the Request content parameter is set. Valid values:    -   Text
    -   Hexadecimal Format |
    |Request content|Common text or hexadecimal format|No|    -   Common text

Common text refers to strings that consist of printable characters.

**Note:** Common text does not support escaping. For example, \\n is considered as two characters \(\\ and n\) rather than the newline character.

    -   Hexadecimal format

If the request content is a byte string that cannot be presented in printable characters, you can convert the byte string to a hexadecimal string that consists of printable characters. Conversion rules: A byte is converted to two hexadecimal characters. For example, `(byte)1` is converted to 01 and `(byte)27` is converted to 1B.

Binary array in the Java format: `{(byte)1, (byte)27}` is converted to 011b or 011B. Hexadecimal characters are not case-sensitive in site monitoring. Enter `"011B"` in the Request content field and set the Request content format parameter to Hexadecimal Format. |
    |match response content format|Radio button|Yes|This parameter takes effect only when the Match response content parameter is set. Valid values: Hexadecimal Format and Text.|
    |Match response content|Common text or hexadecimal format|No|    -   Common text

Common text refers to strings that consist of printable characters.

**Note:** Common text does not support escaping. For example, \\n is considered as two characters \(\\ and n\) rather than the newline character.

    -   Hexadecimal format

If the request content is a byte string that cannot be presented in printable characters, you can convert the byte string to a hexadecimal string that consists of printable characters. Conversion rules: A byte is converted to two hexadecimal characters. For example, `(byte)1` is converted to 01 and `(byte)27` is converted to 1B.

Binary array in the Java format: `{(byte)1, (byte)27}` is converted to 011b or 011B. Hexadecimal characters are not case-sensitive in site monitoring. Enter `"011B"` in the Request content field and set the Request content format parameter to Hexadecimal Format. |

-   DNS

    |Parameter|Setting method|Required|Description|
    |---------|--------------|--------|-----------|
    |Monitor Domain Name|Domain name|Yes|N/A|
    |Type of the DNS record|Radio button|Yes|Valid values: A, MX, NS, CNAME, TXT, and ANY.

Default value: A. |
    |DNS server|IP address of the server|No|If you do not set this parameter, the default DNS server address of the detection point is used. You can enter a domain name or an IP address.|
    |Expected to resolve IP address or domain|Multiple lines of text|No|Each IP address or domain name occupies a line.

The detection is considered successful only when the list of expected values is a subset of the list of DNS results. |

-   POP3

    |Parameter|Setting method|Required|Description|
    |---------|--------------|--------|-----------|
    |Monitor Address|URL|Yes|    -   If the POP3S protocol is used, the URL must contain the pop3s scheme. Example: pop3s://pop3.aliyun.com.
    -   If you enter a URL that does not include a scheme, the default scheme pop3 is added to the URL.
**Note:** The POP3 or POP3S protocol uses TLS for encrypted transmission. |
    |username|Text|Yes|The username and password used for authentication.

Make sure that the specified username and password are correct. Site monitoring sends detection requests in the frequency that you specify. If the username or password is wrong, your account may be blocked by the destination service due to frequent logon failures. |
    |Password|Text|Yes|

-   SMTP

    |Parameter|Setting method|Required|Description|
    |---------|--------------|--------|-----------|
    |Monitor Address|URL|Yes|    -   If the SMTPS protocol is used, the URL must contain the smtps scheme. Example: smtps://smtp.aliyun.com.
    -   If you enter a URL that does not include a scheme, the default scheme smtp is added to the URL.
**Note:** The SMTP or SMTPS client uses the STARTTLS command to negotiate the encryption method with the server. If the secure connection is used, the authentication information is also encrypted. |
    |username|Text|Yes|Used for PLAIN authentication.

Make sure that the specified username and password are correct. Site monitoring sends detection requests in the frequency that you specify. If the username or the password is wrong, your account may be blocked by the destination service due to frequent logon failures. |
    |Password|Text|Yes|

-   FTP

    |Parameter|Setting method|Required|Description|
    |---------|--------------|--------|-----------|
    |Monitor Address|URL|Yes|Example: ftp://smtp.aliyun.com.|
    |Are you anonymous login|Radio button|Yes|    -   Default value: Anonymous Logon.
    -   Authentication Required

If you select this parameter, you must specify the username and password of the FTP server. |
    |username|Text|Yes|The username and password of the FTP server. |
    |Password|Text|Yes|


