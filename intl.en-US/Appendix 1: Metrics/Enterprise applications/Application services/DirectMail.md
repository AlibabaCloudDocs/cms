# DirectMail

This topic describes the metrics for Direct Mail.

-   Set the **Namespace** parameter to **acs\_directmail**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|WEB/API: Maximum Length Exceeded Error QPS|count/min|MAILAGENT\_SENDMAIL\_ERR\_MSGSIZE\_QPS|userId|Value|
|WEB/API: Quota Exceeded Error QPS|count/min|MAILAGENT\_SENDMAIL\_ERR\_QUOTA\_QPS|userId|Value|
|WEB/API: Spam QPS|count/min|MAILAGENT\_SENDMAIL\_ERR\_SPAM\_QPS|userId|Value|
|WEB/API: Email Sent Successfully QPS|count/min|MAILAGENT\_SENDMAIL\_SUCC\_QPS|userId|Value|
|SMTP: Verification Failed QPS|count/min|SMTP\_AUTH\_FAILED\_QPS|userId|Value|
|SMTP: Verification Successful QPS|count/min|SMTP\_AUTH\_SUCC\_QPS|userId|Value|
|SMTP: Maximum Length Exceeded Error QPS|count/min|SMTP\_SENDMAIL\_ERR\_MSGSIZE\_QPS|userId|Value|
|SMTP: Quota Exceeded Error QPS|count/min|SMTP\_SENDMAIL\_ERR\_QUOTA\_QPS|userId|Value|
|SMTP: Spam QPS|count/min|SMTP\_SENDMAIL\_ERR\_SPAM\_QPS|userId|Value|
|SMTP: Email Sent Successfully QPS|count/min|SMTP\_SENDMAIL\_SUCC\_QPS|userId|Value|
|Abnormal Account: Malicious IP Access QPS|count/min|UD\_AUTH\_ERR\_IP\_QPS|userId|Value|
|Abnormal Account: Password Incorrect QPS|count/min|UD\_AUTH\_ERR\_PASSWD\_QPS|userId|Value|
|Abnormal Account: Account Frozen QPS|count/min|UD\_AUTH\_ERR\_STATUS\_QPS|userId|Value|

