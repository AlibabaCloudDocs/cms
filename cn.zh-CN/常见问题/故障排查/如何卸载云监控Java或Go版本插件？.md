# 如何卸载云监控Java或Go版本插件？

如果您需要手动为指定主机安装云监控C++版本插件，且该主机已安装Java或Go版本插件，则需要执行本操作卸载该插件。

## Windows

1.  以Administrator用户登录云监控插件所在主机。

2.  创建.ps1格式文件，例如：test.ps1。

3.  将以下内容拷贝到文件test.ps1中。

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

4.  保存并关闭文件test.ps1。

5.  选中文件test.ps1，单击鼠标右键，选择**使用PowerShell运行**。


## Linux

1.  以root用户登录云监控插件所在主机。

2.  执行以下命令，创建文件，例如：test.sh。

    touch test.sh

3.  执行以下命令，编辑文件test.sh。

    vi test.sh

4.  将以下内容拷贝到文件test.sh中。

    ```
    #!/bin/bash
    
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
    #卸载Java和Go插件
    GOAGENT_ELF_NAME=${CMS_HOME}/CmsGoAgent.${CMS_OS}-${ARCH}
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

5.  按Esc键，输入:wq，再按Enter键，保存并退出文件test.sh。

6.  执行以下命令，执行文件test.sh。

    sh test.sh


