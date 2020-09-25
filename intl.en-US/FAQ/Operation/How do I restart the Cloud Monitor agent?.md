# How do I restart the Cloud Monitor agent?

After you install or configure the Cloud Monitor agent, you must restart it to apply the configuration. This topic describes how to restart the Cloud Monitor agent in Windows and Linux.

## Windows

1.  Log on to the server where the Cloud Monitor agent resides as the administrator.

2.  Go to the C:\\Program Files\\Alibaba\\cloudmonitor directory where the Cloud Monitor agent resides.

3.  Double-click stop.bat to stop the Cloud Monitor agent.

4.  Double-click start.bat to start the Cloud Monitor agent.


## Linux

1.  Log on to the server where the Cloud Monitor agent resides as the root user.

2.  Run the following command to go to the directory of the Cloud Monitor agent:

    cd /usr/local/cloudmonitor

3.  Run the following command to restart the Cloud Monitor agent:

    ./cloudmonitorCtl.sh restart


