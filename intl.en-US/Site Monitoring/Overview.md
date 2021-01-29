# Overview

This topic describes what site monitoring is, its typical scenarios, and supported protocols.

Site monitoring is a monitoring service that allows you to test network connectivity. Site monitoring sends detection requests that simulate real user access from Alibaba Cloud data centers to your site. The following section describes the typical scenarios of using site monitoring.

## Scenarios

Site monitoring is applicable to the following scenarios:

-   Performance analysis

    Create a site monitoring task to obtain the information about the specified site, such as the time taken to resolve the domain name to an IP address, time taken to establish the connection, time taken to receive the first packet, and download time. The information can help you analyze the performance bottlenecks of your service.

-   Competitive analysis

    Monitor your site and competitive sites at the same time by using the selected detection points. Based on the monitoring result, you can compare the quality of your service with that of competitive services.

-   Probe coverage analysis

    Send detection requests from all Alibaba Cloud regions to your site to test the access to your site. Detection requests can be sent from 20 Alibaba Cloud regions.


## Detection protocols

The following table describes the protocols that are supported by site monitoring.

|Protocol|Feature|
|:-------|:------|
|HTTP or HTTPS|Sends HTTP or HTTPS requests to a specific URL or IP address to monitor the URL or IP address.|
|PING|Sends ICMP requests that carry the ping command to a specific URL or IP address to monitor the URL or IP address.|
|TCP|Sends TCP requests to a specific port to monitor the port.|
|UDP|Sends UDP requests to a specific port to monitor the port.|
|DNS|Sends DNS requests to a specific domain to monitor the domain.|
|POP3|Sends POP3 requests to a specific URL or IP address to monitor the URL or IP address.|
|SMTP|Sends SMTP requests to a specific URL or IP address to monitor the URL or IP address.|
|FTP|Sends FTP requests to a specific URL or IP address to monitor the URL or IP address.|

**Note:** For more information about the advanced settings for different protocols, see [Description](/intl.en-US/Site Monitoring/Create a site monitoring task.md).

