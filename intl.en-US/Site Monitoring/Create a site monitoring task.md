# Create a site monitoring task

You can create a site monitoring task to analyze network quality and service performance.

-   An alert contact and an alert group are created. This prerequisite applies if you need to configure alert rules for a site monitoring task. When you create an alert rule, you can select the alert group as the alert notification recipient. For more information, see [Create an alert contact or alert group](/intl.en-US/Alarm service/Alert contacts/Create an alert contact or alert group.md).
-   A callback URL that can be accessed over the Internet is prepared. This prerequisite applies if you need to use alert callbacks. URL callback is enabled as an alert notification method in your existing O&M or notification system.

Site monitoring sends detection requests that simulate real user access from Alibaba Cloud data centers to your site to test and monitor access to your site. Site monitoring is applicable to the following scenarios:

-   Create a site monitoring task to obtain the information about the destination site, such as the time consumed to resolve the domain name to an IP address, establish the connection, receive the first packet, and download data. The information can help you analyze the performance bottlenecks of your service.
-   Monitor the sites of Alibaba Cloud and carriers at the same time by using the selected detection points. Based on the monitoring results, you can compare the quality of Alibaba Cloud services with that of the services provided by the carriers.
-   Send detection requests from all Alibaba Cloud regions to your site to test the access to your site.

## Procedure

1.  Log on to [Cloud Monitor console](https://cms-intl.console.aliyun.com) .

2.  In the left-side navigation pane, choose **New Site Monitor** \> **Site Manage**.

3.  On the Site Monitoring page, click **New Monitoring Task** in the upper-right corner.

4.  On the New Task page, set the parameters.

    |Parameter|Description|
    |---------|-----------|
    |**Monitor Type**|The protocol used to monitor the site. Valid values: HTTP\(S\), PING, TCP, UDP, DNS, SMTP, POP3, and FTP.|
    |**IP Probe Type**|The IP address type of the detection point. Valid values: IPv4 and IPv6.|
    |**Task Name**|The name of the site monitoring task. The value must be 4 to 100 characters in length and can contain letters, digits, and underscores \(\_\).|
    |**Monitor Address**|The address of the site to be monitored. You can specify multiple addresses at a time. Each address occupies a line. After you save the configurations, Cloud Monitor generates a site monitoring task for each specified site address.|
    |**Monitoring frequency**|The interval at which detection requests are sent. Valid values: 1 min, 5 minutes, 15 minutes, 30 minutes, and 60 minutes. For example, if you select 1 min, a detection point sends a detection request to the monitored site every minute.|
    |**Advanced Settings**|The advanced settings for the selected protocol. For more information, see [Description](#section_08r_0oc_dac).|

5.  Select detection points.

    **Probe points advanced options**: allows you to customize detection points by specifying the carrier and region.

6.  Configure an alert rule.

    |Parameter|Description|
    |---------|-----------|
    |**Availability**|The availability-related metric for triggering alerts. Valid values:    -   Number of probe points available

The value is the number of detection results in which the status code is smaller than 400 within a monitoring period.

    -   Available probe point ratio

The value is the percentage of detection results in which the status code is smaller than 400 to all detection results within a monitoring period.

    -   Any Status Code \(Independent Alert\)
    -   All Status Code \(Combined Alert\) |
    |**Average response time**|The average response time of all detection points within a monitoring period.|
    |**Triggered when threshold is exceeded for**|The condition for sending alert notifications. An alert notification is sent only if the threshold is consecutively exceeded for the specified number of times. No alert notification is sent if the threshold is occasionally exceeded. This prevents false alerts caused by occasional network jitters.|
    |**Contact Group**|The alert group to which alert notifications are sent.|
    |**Notification Methods**|The methods that are used to send alert notifications.|
    |**Channel Silence Time**|The interval at which an alert notification is sent before the alert is cleared.|
    |**Effective Time**|The time period during which the alert rule is effective. Cloud Monitor sends alert notifications only within the effective period. Cloud Monitor only records alerts if the alerts are generated in other time periods.|
    |**Alert Callback**|The callback URL that can be accessed over the Internet. Advanced settings for different protocols|

7.  Click **Create**.


## Description

The following tables list the advanced settings for different protocols.

-   HTTP or HTTPS

    |Parameter|Setting method|Required|Description|
    |---------|--------------|--------|-----------|
    |Monitor Address|URL|Yes|    -   The URL of the site to be monitored. If the HTTPS protocol is used, the URL must contain the https scheme. Example: `https://www.baidu.com`.
    -   If you enter a URL that does not have a scheme, the default scheme http or https is added to the URL. |
    |Request content|Enter form data or JSON objects.|No|The body of the request. If the request is in the JSON format, you must enclose JSON objects in braces \{\} in the request body. Otherwise, the request body is parsed as form data.|
    |Request method|Select an option.|Yes|The request method. Valid values:

    -   GET
    -   POST
    -   HEAD
Default value: GET. |
    |Match response method|Select an option.|Yes|Specifies whether to generate an alert based on whether the response matches the expected or unexpected content. If you specify the expected or unexpected content, site monitoring checks whether the first 64 KB of the response body matches the expected or unexpected content and determines whether to generate an alert based on the matching result. Valid values:

    -   Alert if the matching content is included.
    -   Alert if the matching content is not included.
Site monitoring determines whether to send an alert notification based on the match response method.

Specifies the expected or unexpected content to be matched with the response. The matching content must be in English. |
    |Match response content|Enter the text.|No|
    |HTTP request header|Enter multiple lines of text.|No|The HTTP request header. The HTTP request header consists of key-value pairs. Each key-value pair occupies a line. The key and value in each pair are separated by a colon \(:\). Site monitoring adds the following preset fields to the HTTP request header:

    -   `Host:${Domain name in the address of the monitored site}`
    -   `Pragma:no-cache`
    -   `Cache-Control:no-cache`
    -   `User-Agent:Chrome/57`
    -   `Accept: */*`
If the request body is a form, the request header also includes the following field:

`Content-Type: application/x-www-form-urlencoded;charset=UTF-8`

If your HTTP request header contains one or more of the preceding fields, the fields are overwritten by your settings.

**Note:** Site monitoring converts the keys that you specify in the request header to the canonical format of MIME header based on the HTTP protocol and the following rules:

    -   The first letter and the letter next to a hyphen \(-\) are converted to uppercase letters. For example, accept-encoding is converted to Accept-Encoding.
    -   If a key contains a space or invalid characters, the key remains unchanged. |
    |Cookie|Enter an HTTP cookie.|No|The HTTP cookie.|
    |HTTP Authentication Username|Enter a username.|No|The username and password used for basic HTTP authentication.|
    |HTTP Authentication Password|Enter a password.|No|
    |Certificate verification|Select or clear the check box.|No|Specifies whether server name indication \(SNI\) is supported. By default, the check box is cleared, indicating that SNI is not supported.|
    |Unfollow Redirect|Select or clear the check box.|No|Specifies whether to send detection requests to the new URL if status code 301 or 302 that indicates a redirection is returned. By default, the check box is cleared, indicating that Cloud Monitor sends detection requests to the new URL.|

-   PING

    |Parameter|Setting method|Required|Description|
    |---------|--------------|--------|-----------|
    |Monitor Address|Enter one or more domain names or IP addresses.|Yes|N/A|
    |Number of ping packets|Enter a positive integer.|Yes|The number of times that the site is pinged. Default value: 20. Valid values: 1 to 40.|

-   TCP or UDP

    |Parameter|Setting method|Required|Description|
    |---------|--------------|--------|-----------|
    |Monitor Address|Enter one or more domain names or IP addresses.|Yes|-|
    |Request content format|Select an option.|Yes|The format of the request body. This parameter takes effect only if the Request content parameter is set. Valid values:    -   Text
    -   Hexadecimal Format |
    |Request content|Enter strings or hexadecimal strings.|No|    -   Text

If the Request content format parameter is set to Text, enter strings that consist of printable characters in the Request content field.

**Note:** You cannot escape special characters in strings. For example, \\n is considered as two characters \(\\ and n\) rather than the newline character.

    -   Hexadecimal Format

If the Request content format parameter is set to Hexadecimal Format, enter hexadecimal strings to which the non-printable bytes are converted in the Request content field. A byte is converted to two hexadecimal characters. For example, `(byte)1` is converted to 01 and `(byte)27` is converted to 1B.

Assume that the request content contains a binary array in the Java format. For example, the binary array `{(byte)1, (byte)27}` can be converted to 011b or 011B. Hexadecimal characters generated after conversion are not case-sensitive in site monitoring. Then, you can enter `"011B"` in the Request content field and set the Request content format parameter to Hexadecimal Format. |
    |match response content format|Select an option.|Yes|The format of the expected or unexpected content to be matched with the response. This parameter takes effect only if the Match response content parameter is set. Valid values: Hexadecimal Format and Text.|
    |Match response content|Enter strings or hexadecimal strings.|No|    -   Text

If the Request content format parameter is set to Text, enter strings that consist of printable characters in the Request content field.

**Note:** You cannot escape special characters in strings. For example, \\n is considered as two characters \(\\ and n\) rather than the newline character.

    -   Hexadecimal Format

If the Request content format parameter is set to Hexadecimal Format, enter hexadecimal strings to which the non-printable bytes are converted in the Request content field. A byte is converted to two hexadecimal characters. For example, `(byte)1` is converted to 01 and `(byte)27` is converted to 1B.

Assume that the request content contains a binary array in the Java format. For example, the binary array `{(byte)1, (byte)27}` can be converted to 011b or 011B. Hexadecimal characters generated after conversion are not case-sensitive in site monitoring. Then, you can enter `"011B"` in the Request content field and set the Request content format parameter to Hexadecimal Format. |

-   DNS

    |Parameter|Setting method|Required|Description|
    |---------|--------------|--------|-----------|
    |Monitor Domain Name|Enter one or more domain names.|Yes|N/A|
    |Type of the DNS record|Select an option.|Yes|The type of the Domain Name System \(DNS\) record. Valid values: A, MX, NS, CNAME, TXT, and ANY.

Default value: A. |
    |DNS server|Enter the domain name or IP address of the DNS server.|No|The domain name or IP address of the DNS server. If you do not set this parameter, the domain name or IP address of the default DNS server is used. You can enter a domain name or an IP address.|
    |Expected to resolve IP address or domain|Enter multiple lines of text.|No|The domain names or IP addresses that are expected to be obtained after DNS resolution. Each IP address or domain name occupies a line.

The DNS resolution is considered successful only if the IP addresses or domain names obtained after DNS resolution include the expected IP addresses or domain names. |

-   POP3 or POP3S

    |Parameter|Setting method|Required|Description|
    |---------|--------------|--------|-----------|
    |Monitor Address|URL|Yes|    -   The URL of the site to be monitored. If the POP3S protocol is used, the URL must contain the pop3s scheme. Example: pop3s://pop3.aliyun.com.
    -   If you enter a URL that does not include a scheme, the default scheme pop3 is added to the URL.
**Note:** The POP3S protocol uses TLS for encrypted transmission. |
    |username|Enter a username.|Yes|The username and password used for authentication.

Make sure that the specified username and password are correct. If the username or the password is invalid, your account may be blocked by the monitored site due to frequent logon failures. |
    |Enter a password.|Enter a password.|Yes|

-   SMTP or SMTPS

    |Parameter|Setting method|Required|Description|
    |---------|--------------|--------|-----------|
    |Monitor Address|URL|Yes|    -   The URL of the site to be monitored. If the SMTPS protocol is used, the URL must contain the smtps scheme. Example: smtps://smtp.aliyun.com.
    -   If you enter a URL that does not include a scheme, the default scheme smtp is added to the URL.
**Note:** The SMTPS protocol uses the STARTTLS command to negotiate the encryption method with the server. If the secure connection is used, the authentication information is also encrypted. |
    |username|Enter a username.|Yes|The username and password used for PLAIN authentication.

Make sure that the specified username and password are correct. If the username or the password is wrong, your account may be blocked by the monitored site due to frequent logon failures. |
    |Password|Enter a password.|Yes|

-   FTP

    |Parameter|Setting method|Required|Description|
    |---------|--------------|--------|-----------|
    |Monitor Address|URL|Yes|The URL of the site to be monitored. Example: ftp://smtp.aliyun.com.|
    |Are you anonymous login|Select an option.|Yes|    -   Specifies whether to allow anonymous logon. Default value: Anonymous Logon.
    -   Authentication Required

If you select Authentication Required, you must specify the username and password used for authentication. |
    |username|Enter a username.|Yes|The username and password used for authentication. |
    |Password|Enter a password.|Yes|


