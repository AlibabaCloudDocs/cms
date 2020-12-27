# What does status code 610 mean?

This topic describes the meaning of status code 610 returned by Cloud Monitor.

Status code 610 indicates an HTTP connection timeout.

Cloud Monitor monitors the status of your site by sending HTTP requests to the site. After Cloud Monitor sends an HTTP request, Cloud Monitor determines that a connection timeout occurs if no response is received within 5 seconds. In this case, Cloud Monitor returns status code 610.

We recommend that you take measures, for example, increase the number of retry times and configure alerts based on combined conditions, to improve the alert accuracy.

