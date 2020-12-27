# How do I uninstall the Java agent or GoLang agent of Cloud Monitor?

If you want to manually install the C++ agent of Cloud Monitor on a specific host on which the Java agent or GoLang agent of Cloud Monitor is installed, you must first uninstall the Java agent or GoLang agent. This topic describes how to uninstall the Java agent or GoLang agent of Cloud Monitor.

## Windows

1.  Log on to the host where the Java agent or GoLang agent resides as the administrator.

2.  Create a .ps1 file, such as the test.ps1 file.

3.  Copy the following content to the test.ps1 file:

    ```
    if([System.Environment]::Is64BitOperatingSystem -eq $true)
    {
        $CMS_ARCH="amd64"
        $ARGUS_ARCH="win64"
    }else
    {
        $CMS_ARCH="386"
        $ARGUS_ARCH="win32"
    }
    
    $dest_path_prefix="C:\Program Files\Alibaba"
    $dest_path="$dest_path_prefix\cloudmonitor"
    
    echo "the current arch is $CMS_ARCH"
    
    $go_dest_file="CmsGoAgent.windows-$CMS_ARCH.exe"
    $argus_dest_file="cloudmonitor_$ARGUS_ARCH.zip"
    $downloadpath="Argus/$CMS_VERSION/$argus_dest_file"
    
    if (Test-Path "$dest_path\wrapper\bin\AppCommand.bat")
    {
       echo "old java cloudmonitor already installed - remove it..."
       & "$dest_path\wrapper\bin\AppCommand.bat" remove
       rm -Force -Recurse "$dest_path"
    }
    if (Test-Path "C:\Program Files (x86)\Alibaba\cloudmonitor\wrapper\bin\AppCommand.bat" )
    {
        echo "old java cloudmonitor already installed - remove it..."
        & "C:\Program Files (x86)\Alibaba\cloudmonitor\wrapper\bin\AppCommand.bat" remove
        rm -Force -Recurse "C:\Program Files (x86)\Alibaba\cloudmonitor"
    }
    
    if (Test-Path "$dest_path\$go_dest_file")
    {
        "echo remove go-agent"
        & "$dest_path\$go_dest_file" stop
        & "$dest_path\$go_dest_file" uninstall
    }
    ```

4.  Save and close the test.ps1 file.

5.  Right-click the test.ps1 file and select **Run with PowerShell**.


## Linux

1.  Log on to the host where the Java agent or GoLang agent resides as the root user.

2.  Create a script file. For example, run the following command to create the test.sh file:

    touch test.sh

3.  Run the following command to open the test.sh file:

    vi test.sh

4.  Copy the following content to the test.sh file:

    ```
    #! /bin/bash
    
    if [ -z "${CMS_HOME}" ]; then
      CMS_HOME_PREFIX="/usr/local"
      if [ -f /etc/os-release -a ! -z "`egrep -i coreos /etc/os-release`" ];then
        CMS_HOME_PREFIX="/opt"
      fi
    fi
    CMS_HOME="${CMS_HOME_PREFIX}/cloudmonitor"
    
    if [ `uname -m` = "x86_64" ]; then
        ARCH="amd64"
        ARGUS_ARCH="64"
    else
        ARCH="386"
        ARGUS_ARCH="32"
    fi
    
    case `uname -s` in
      Linux)
        CMS_OS="linux"
        ;;
      *)
        echo "Unsupported OS: $(uname -s)"
        exit 1
        ;;
    esac
    
    DEST_START_FILE=${CMS_HOME}/cloudmonitorCtl.sh
    # Uninstall the Java agent and GoLang agent.
    GOAGENT_ELF_NAME=${CMS_HOME}/CmsGoAgent. ${CMS_OS}-${ARCH}
    if [ -d ${CMS_HOME} ] ; then
      if [ -f ${DEST_START_FILE} ];then
        ${DEST_START_FILE} stop
      fi
      if [ -f ${CMS_HOME}/wrapper/bin/cloudmonitor.sh ] ; then
        ${CMS_HOME}/wrapper/bin/cloudmonitor.sh remove;
        rm -rf ${CMS_HOME};
      fi
      if [ -f ${GOAGENT_ELF_NAME} ]; then
        ${GOAGENT_ELF_NAME} stop
        rm -rf ${CMS_HOME}
      fi
    fi
    ```

5.  Press the Esc key, enter :wq, and then press the Enter key to save and close the test.sh file.

6.  Run the following command to run the test.sh file:

    sh test.sh


