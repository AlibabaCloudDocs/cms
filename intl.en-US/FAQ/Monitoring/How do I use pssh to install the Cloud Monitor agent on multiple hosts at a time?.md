# How do I use pssh to install the Cloud Monitor agent on multiple hosts at a time?

This topic describes how to use pssh to install the Cloud Monitor agent on multiple hosts at a time.

## Introduction to pssh

pssh is a tool that allows you to perform operations on multiple hosts at the same time. pssh is written in Python and is suitable for performing repetitive operations on no more than 30 hosts at the same time. For example, you can use pssh to install software, stop a process, or download a file on multiple hosts at the same time.

## Install the Cloud Monitor agent on a single host

`**bash**-c "$(curl http://cloudmonitor-agent.oss-cn-hangzhou.aliyuncs.com/release/install.sh)"`

## Install the Cloud Monitor agent on multiple hosts at the same time by using pssh

-   **Install pssh**
    1.  Install Python 2.4 or a later version.
    2.  Install pssh.

        ```
         wget https://pypi.python.org/packages/source/p/pssh/pssh-2.3.1.tar.gz
         tar zxf pssh-2.3.1.tar.gz
         cd pssh-2.3.1
         python setup.py install 
        							
        ```

-   **Add the IP addresses and ports of the hosts where you want to install the Cloud Monitor agent to the ip.txt file**
    1.  Open the ip.txt file.
    2.  Add the IP addresses and ports of the hosts to the ip.txt file in the format of user@ip:port. Each host occupies a row. The default port 22 is used if you do not specify the port for a host.
    3.  Make sure that the user that you specify for a host in the ip.txt file has the sudo permissions on the host.
    4.  Make sure that the same password is configured on the hosts. Alternatively, you can configure mutual trust between the host where you run the pssh tool and the hosts where you want to install the Cloud Monitor agent to allow password-free logons.
-   **Run the pssh tool to install the Cloud Monitor agent on the specified hosts at the same time**

    `pssh -h ip.txt -A -i bash -c "$(curl http://cloudmonitor-agent.oss-cn-hangzhou.aliyuncs.com/release/install.sh)"`

    -h: the file that contains the IP addresses and ports of the hosts where you want to install the Cloud Monitor agent.

    -A: the password used to log on to the hosts. You do not need to specify this parameter if you have configured mutual trust between the host where you run the pssh tool and the hosts where you want to install the Cloud Monitor agent.

    -i: the command used to install the Cloud Monitor agent.

-   **Check whether the Cloud Monitor agent is installed on the hosts**

    `pssh -h ip.txt -A -i"/usr/local/cloudmonitor/wrapper/bin/cloudmonitor.sh status"`


