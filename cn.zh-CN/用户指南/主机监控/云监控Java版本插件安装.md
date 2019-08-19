# 云监控Java版本插件安装 {#concept_d5f_vhv_vdb .concept}

## Linux插件安装说明 {#section_vhm_3cf_xdb .section}

**常用命令**

``` {#codeblock_eta_ges_cqs}
# 运行状态
/usr/local/cloudmonitor/wrapper/bin/cloudmonitor.sh status

# 启动
/usr/local/cloudmonitor/wrapper/bin/cloudmonitor.sh start

# 停止
/usr/local/cloudmonitor/wrapper/bin/cloudmonitor.sh stop

# 重启
/usr/local/cloudmonitor/wrapper/bin/cloudmonitor.sh restart

# 卸载
/usr/local/cloudmonitor/wrapper/bin/cloudmonitor.sh remove && \
rm -rf /usr/local/cloudmonitor
```

**安装命令**

直接复制以下命令后在服务器上使用Root权限运行即可。

**华北1 青岛 cn-qingdao**

``` {#codeblock_nlw_hir_7pl}



REGION_ID=cn-qingdao VERSION=1.3.7 \
bash -c "$(curl https://cms-agent-cn-qingdao.oss-cn-qingdao-internal.aliyuncs.com/release/cms_install_for_linux.sh)"
```

**华北2 北京 cn-beijing**

``` {#codeblock_13u_acx_bri}



REGION_ID=cn-beijing VERSION=1.3.7 \
bash -c "$(curl https://cms-agent-cn-beijing.oss-cn-beijing-internal.aliyuncs.com/release/cms_install_for_linux.sh)"
```

**华北3 张家口 cn-zhangjiakou**

``` {#codeblock_o6j_cfs_94v}



REGION_ID=cn-zhangjiakou VERSION=1.3.7 \
bash -c "$(curl https://cms-agent-cn-zhangjiakou.oss-cn-zhangjiakou-internal.aliyuncs.com/release/cms_install_for_linux.sh)"
```

**华北5 呼和浩特 cn-huhehaote**

``` {#codeblock_44m_3th_k00}



REGION_ID=cn-huhehaote VERSION=1.3.7 \
bash -c "$(curl https://cms-agent-cn-huhehaote.oss-cn-huhehaote-internal.aliyuncs.com/release/cms_install_for_linux.sh)"
```

**华东1 杭州 cn-hangzhou**

``` {#codeblock_zrp_pb7_ed3}



REGION_ID=cn-hangzhou VERSION=1.3.7 \
bash -c "$(curl https://cms-agent-cn-hangzhou.oss-cn-hangzhou-internal.aliyuncs.com/release/cms_install_for_linux.sh)"
```

**华东2 上海 cn-shanghai**

``` {#codeblock_dio_953_i3c}



REGION_ID=cn-shanghai VERSION=1.3.7 \
bash -c "$(curl https://cms-agent-cn-shanghai.oss-cn-shanghai-internal.aliyuncs.com/release/cms_install_for_linux.sh)"
```

**华南1 深圳 cn-shenzhen**

``` {#codeblock_1d6_sbb_tpe}



REGION_ID=cn-shenzhen VERSION=1.3.7 \
bash -c "$(curl https://cms-agent-cn-shenzhen.oss-cn-shenzhen-internal.aliyuncs.com/release/cms_install_for_linux.sh)"
```

**中国香港 香港 cn-hongkong**

``` {#codeblock_i9r_009_0sh}



REGION_ID=cn-hongkong VERSION=1.3.7 \
bash -c "$(curl https://cms-agent-cn-hongkong.oss-cn-hongkong-internal.aliyuncs.com/release/cms_install_for_linux.sh)"
```

**美国西部1 硅谷 us-west-1**

``` {#codeblock_oai_67t_2pk}



REGION_ID=us-west-1 VERSION=1.3.7 \
bash -c "$(curl https://cms-agent-us-west-1.oss-us-west-1-internal.aliyuncs.com/release/cms_install_for_linux.sh)"
```

**美国东部1 弗吉尼亚 us-east-1**

``` {#codeblock_6zc_vrj_5dn}



REGION_ID=us-east-1 VERSION=1.3.7 \
bash -c "$(curl https://cms-agent-us-east-1.oss-us-east-1-internal.aliyuncs.com/release/cms_install_for_linux.sh)"
```

**亚太东南1 新加坡 ap-southeast-1**

``` {#codeblock_or6_th2_v9m}



REGION_ID=ap-southeast-1 VERSION=1.3.7 \
bash -c "$(curl https://cms-agent-ap-southeast-1.oss-ap-southeast-1-internal.aliyuncs.com/release/cms_install_for_linux.sh)"
```

**亚太东南2 悉尼 ap-southeast-2**

``` {#codeblock_nf8_o3p_bj0}



REGION_ID=ap-southeast-2 VERSION=1.3.7 \
bash -c "$(curl https://cms-agent-ap-southeast-2.oss-ap-southeast-2-internal.aliyuncs.com/release/cms_install_for_linux.sh)"
```

**亚太东南3 吉隆坡 ap-southeast-3**

``` {#codeblock_seq_7jd_qq1}



REGION_ID=ap-southeast-3 VERSION=1.3.7 \
bash -c "$(curl https://cms-agent-ap-southeast-3.oss-ap-southeast-3-internal.aliyuncs.com/release/cms_install_for_linux.sh)"
```

**亚太东南5 雅加达 ap-southeast-5**

``` {#codeblock_ujp_vvz_gx2}



REGION_ID=ap-southeast-5 VERSION=1.3.7 \
bash -c "$(curl https://cms-agent-ap-southeast-5.oss-ap-southeast-5-internal.aliyuncs.com/release/cms_install_for_linux.sh)"
```

**亚太东北1 东京 ap-northeast-1**

``` {#codeblock_g8e_05i_vxh}



REGION_ID=ap-northeast-1 VERSION=1.3.7 \
bash -c "$(curl https://cms-agent-ap-northeast-1.oss-ap-northeast-1-internal.aliyuncs.com/release/cms_install_for_linux.sh)"
```

**亚太南部1 孟买 ap-south-1**

``` {#codeblock_g2w_kpf_w3y}



REGION_ID=ap-south-1 VERSION=1.3.7 \
bash -c "$(curl https://cms-agent-ap-south-1.oss-ap-south-1-internal.aliyuncs.com/release/cms_install_for_linux.sh)"
```

**欧洲中部1 法兰克福 eu-central-1**

``` {#codeblock_hno_sdt_vqa}



REGION_ID=eu-central-1 VERSION=1.3.7 \
bash -c "$(curl https://cms-agent-eu-central-1.oss-eu-central-1-internal.aliyuncs.com/release/cms_install_for_linux.sh)"
```

**欧洲西部 英国伦敦 eu-west-1**

``` {#codeblock_bmk_6fd_ovc}



REGION_ID=eu-west-1 VERSION=1.3.7 \ bash -c "$(curl https://cms-agent-eu-west-1.oss-eu-west-1-internal.aliyuncs.com/release/cms_install_for_linux.sh)"
```

**中东东部 迪拜 me-east-1**

``` {#codeblock_7j8_m9u_1tx}



REGION_ID=me-east-1 VERSION=1.3.7 \
bash -c "$(curl https://cms-agent-me-east-1.oss-me-east-1-internal.aliyuncs.com/release/cms_install_for_linux.sh)"
```

**华东1金融云 杭州 cn-hangzhou**

``` {#codeblock_o6t_cnq_5uk}



REGION_ID=cn-hangzhou VERSION=1.3.7 \
bash -c "$(curl https://cms-agent-cn-hangzhou.oss-cn-hangzhou-internal.aliyuncs.com/release/cms_install_for_linux.sh)"
```

**华东2金融云 上海 cn-shanghai-finance-1**

``` {#codeblock_l7k_oia_xcc}



REGION_ID=cn-shanghai-finance-1 VERSION=1.3.7 \
bash -c "$(curl https://cms-agent-cn-shanghai-finance-1.oss-cn-shanghai-finance-1-pub-internal.aliyuncs.com/release/cms_install_for_linux.sh)"
```

**华南1金融云 深圳 cn-shenzen-finance-1**

``` {#codeblock_cws_280_uuc}



REGION_ID=cn-shenzhen-finance-1 VERSION=1.3.7 \
bash -c "$(curl http://cms-agent-cn-shenzhen-finance-1.oss-cn-shenzhen-finance-1-internal.aliyuncs.com/release/cms_install_for_linux.sh)"
```

## Windows插件安装说明 {#section_fxr_wdf_xdb .section}

**安装步骤**

1.  根据系统情况，下载云监控插件[64位版本插件](http://cms-download.aliyun.com/release/1.3.7/windows64/agent-windows64-1.3.7-package.zip)或[32位版本插件](http://cms-download.aliyun.com/release/1.3.7/windows32/agent-windows32-1.3.7-package.zip)。
2.  在C:/Program Files/Alibaba路径下新建文件夹cloudmonitor。
3.  解压到C:/Program Files/Alibaba/cloudmonitor目录。
4.  使用管理员权限双击运行安装云监控C:/Program Files/Alibaba/cloudmonitor/wrapper/bin/InstallApp-NT.bat。
5.  使用管理员权限双击运行启动云监控C:/Program Files/Alibaba/cloudmonitor/wrapper/bin/StartApp-NT.bat。
6.  安装完成后，可以通过Windows服务面板来查看、启动、停止云监控服务（Cloud Monitor Application）。

**卸载步骤**

1.  使用Windows服务面板停止云监控服务。
2.  通过管理员权限运行C:/Program Files/Alibaba/cloudmonitor/wrapper/bin/UninstallApp-NT.bat来删除云监控服务。
3.  到安装目录删除整个目录C:/Program Files/Alibaba/cloudmonitor。

**无公网下载**

如果没有公网可以通过内网地址下载，例如青岛64位安装包下载地址为：[http://cms-agent-cn-qingdao.oss-cn-qingdao.aliyuncs.com/release/1.3.7/windows64/agent-windows64-1.3.7-package.zip](http://cms-agent-cn-qingdao.oss-cn-qingdao.aliyuncs.com/release/1.3.7/windows64/agent-windows64-1.3.7-package.zip)

-   可以通过修改两处cn-qingdao切换到其他region下载地址
-   可以通过将两处windows64修改为windows32来切换到32位版本
-   可以通过修改两处1.3.7切换到其他版本

## **安全配置说明** {#section_s5t_313_p2b .section}

以下是云监控插件与服务端交互用到的端口，这些端口被安全软件禁用后，会导致监控数据采集异常，如果您的ECS服务器对安全要求较高，需要针对具体IP地址放行，可以将下列IP加入白名单。

**说明：** 未来随着云监控版本的更新维护，可能会加入更多的IP地址或变更IP地址，为简化防火墙规则的配置，可以直接配置允许100.100网段的出方向，这个网段是阿里云内网保留网段，用于提供阿里云官方服务。

|Region|IP|方向|描述|
|------|--|--|--|
|cn-hangzhou 华东 1 杭州|100.100.19.43:3128|出方向|监控配置管理等管控类操作|
|100.100.45.73:80|出方向|收集监控数据到云监控服务端|
|cn-beijing 华北 2 北京|100.100.18.22:3128|出方向|监控配置管理等管控类操作|
|100.100.18.50:80|出方向|收集监控数据到云监控服务端|
|cn-qingdao 华北 1 青岛|100.100.36.102:3128|出方向|监控配置管理等管控类操作|
|100.100.15.23:80|出方向|收集监控数据到云监控服务端|
|cn-shenzhen 华南 1 深圳|100.100.0.13:3128|出方向|监控配置管理等管控类操作|
|100.100.0.31:80|出方向|收集监控数据到云监控服务端|
|cn-hongkong 中国香港 香港|100.103.0.47:3128|出方向|监控配置管理等管控类操作|
|100.103.0.45:80|出方向|收集监控数据到云监控服务端|
|cn-huhehaote 华北 5 呼和浩特|100.100.80.135:8080|出方向|监控配置管理等管控类操作|
|100.100.80.12:80|出方向|收集监控数据到云监控服务端|
|cn-zhangjiakou 华北 3 张家口|100.100.80.92:8080|出方向|监控配置管理等管控类操作|
|100.100.0.19:80|出方向|收集监控数据到云监控服务端|
|cn-shanghai 华东 2 上海|100.100.36.11:3128|出方向|监控配置管理等管控类操作|
|100.100.36.6:80|出方向|收集监控数据到云监控服务端|
|cn-chengdu 西南 1 成都|100.100.80.229:8080|出方向|监控配置管理等管控类操作|
|100.100.80.14:80|出方向|收集监控数据到云监控服务端|
|us-east-1 美国东部 1 弗吉尼亚|100.103.0.95:3128|出方向|监控配置管理等管控类操作|
|100.103.0.94:80|出方向|收集监控数据到云监控服务端|
|us-west-1 美国西部 1 硅谷|100.103.0.95:3128|出方向|监控配置管理等管控类操作|
|100.100.29.7:80|出方向|收集监控数据到云监控服务端|
|eu-central-1 欧洲中部 1 德国 法兰克福|100.100.80.241:8080|出方向|监控配置管理等管控类操作|
|100.100.80.72:80|出方向|收集监控数据到云监控服务端|
|eu-west-1 英国 伦郭|100.100.0.3:8080|出方向|监控配置管理等管控类操作|
|100.100.0.2:80|出方向|收集监控数据到云监控服务端|
|ap-southeast-1 亚太东南 1 新加坡|100.100.30.20:3128|出方向|监控配置管理等管控类操作|
|100.100.103.7:80|出方向|收集监控数据到云监控服务端|
|ap-southeast-2 亚太东南 2 澳大利亚 悉尼|100.100.80.92:8080|出方向|监控配置管理等管控类操作|
| 100.100.80.13:80

 \[47.91.39.6:443\]

 |出方向|收集监控数据到云监控服务端|
|ap-southeast-3 亚太东南 3 吉隆坡|100.100.80.153:8080|出方向|监控配置管理等管控类操作|
|100.100.80.140:80|出方向|收集监控数据到云监控服务端|
|ap-southeast-5亚太东南 5 雅加达|100.100.80.160:8080|出方向|监控配置管理等管控类操作|
|100.100.80.180:80|出方向|收集监控数据到云监控服务端|
|me-east-1 中东东部 1 迪拜|100.100.80.142:8080|出方向|监控配置管理等管控类操作|
| 100.100.80.151:80

 \[47.91.99.5:443\]

 |出方向|收集监控数据到云监控服务端|
|ap-northeast-1 亚太东北 1 日本 东京|100.100.80.184:8080|出方向|监控配置管理等管控类操作|
| 100.100.80.137:80

 \[47.91.8.7:443\]

 |出方向|收集监控数据到云监控服务端|
|ap-south-1 亚太南部 1 孟买|100.100.80.152:8080|出方向|监控配置管理等管控类操作|
|100.100.80.66:80|出方向|收集监控数据到云监控服务端|

## 资源消耗 {#section_oh3_r3f_xdb .section}

-   插件安装包大小：75M。
-   安装后大小：200M。
-   内存：64M。
-   CPU：1%以下。
-   网络：使用内网网络，不消耗公网流量。

## 常见问题 {#section_vv2_nff_xdb .section}

-   云监控日志位置：
    -   Linux：/usr/local/cloudmonitor/logs
    -   Windows：C:/Program Files/Alibaba/cloudmonitor/logs

-   插件占用的端口和我的业务端口冲突怎么办？

    1.  修改云监控配置来更换端口范围，文件位置：/usr/local/cloudmonitor/wrapper/conf/wrapper.conf
    2.  重启云监控
    ``` {#codeblock_wbt_cw0_bhq}
    
    wrapper.port.min=40000
    wrapper.port.max=41000
    wrapper.jvm.port.min=41001
    wrapper.jvm.port.max=42000
    ```


