# DescribeSiteMonitorISPCityList

调用DescribeSiteMonitorISPCityList接口查询创建任务的探测点列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeSiteMonitorISPCityList&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeSiteMonitorISPCityList|要执行的操作，取值：DescribeSiteMonitorISPCityList。 |
|Isp|String|否|中国移动|探测的运营商名称或ID。运营商名称支持模糊查询。 |
|City|String|否|北京市|探测的城市名称或ID。城市名称支持模糊查询。 |
|IPV6|Boolean|否|false|IPv6探针。取值：

 -   true：过滤出所有IPv6探针。
-   false：不过滤IPv6探针。 |
|IPV4|Boolean|否|true|IPv4探针。取值：

 -   true：过滤出所有IPv4探针。
-   false：不过滤IPv4探针。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|RequestId|String|848EF34A-FD9F-48A6-879F-414279ED4F26|请求ID。 |
|Message|String|successful|返回信息。 |
|IspCityList|Array of IspCity| |探测点列表。 |
|IspCity| | | |
|City|String|738|城市ID。 |
|CityName.en|String|Yantai|城市名称（英文）。 |
|CityName.zh\_CN|String|烟台市|城市名称（简体中文）。 |
|Country|String|629|国家代码。 |
|Country.en|String|China|国家（英文）。 |
|Country.zh\_CN|String|中国|国家（简体中文）。 |
|IPV4ProbeCount|String|2|IPv4探针数量。 |
|IPV6ProbeCount|String|3|IPv6探针数量。 |
|Isp|String|232|运营商ID。 |
|IspName.en|String|China-Mobile|运营商名称（英文）。 |
|IspName.zh\_CN|String|中国移动|运营商名称（简体中文）。 |
|Region|String|200|省份代码。 |
|Region.en|String|Shandong|省份（英文）。 |
|Region.zh\_CN|String|山东省|省份（简体中文）。 |
|Success|String|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeSiteMonitorISPCityList
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeSiteMonitorISPCityListResponse>
		  <Message>successful</Message>
		  <IspCityList>
			    <IspCity>
				      <Country.zh_CN>中国</Country.zh_CN>
				      <CityName.en>Yantai</CityName.en>
				      <Region.zh_CN>山东省</Region.zh_CN>
				      <Isp>5</Isp>
				      <Region>200</Region>
				      <Country>629</Country>
				      <City>428</City>
				      <IspName.en>China-Mobile</IspName.en>
				      <IspName.zh_CN>中国移动</IspName.zh_CN>
				      <Region.en>Shandong</Region.en>
				      <Country.en>China</Country.en>
				      <IPV6ProbeCount>0</IPV6ProbeCount>
				      <IPV4ProbeCount>2</IPV4ProbeCount>
				      <CityName.zh_CN>烟台市</CityName.zh_CN>
			    </IspCity>
			    <IspCity>
				      <Country.zh_CN>中国</Country.zh_CN>
				      <CityName.en>Xian</CityName.en>
				      <Region.zh_CN>陕西省</Region.zh_CN>
				      <Isp>507</Isp>
				      <Region>28</Region>
				      <Country>629</Country>
				      <City>311</City>
				      <IspName.en>DrPeng</IspName.en>
				      <IspName.zh_CN>鹏博士</IspName.zh_CN>
				      <Region.en>Shaanxi</Region.en>
				      <Country.en>China</Country.en>
				      <IPV6ProbeCount>0</IPV6ProbeCount>
				      <IPV4ProbeCount>2</IPV4ProbeCount>
				      <CityName.zh_CN>西安市</CityName.zh_CN>
			    </IspCity>
			    <IspCity>
				      <Country.zh_CN>中国</Country.zh_CN>
				      <CityName.en>Jingzhou</CityName.en>
				      <Region.zh_CN>湖北省</Region.zh_CN>
				      <Isp>5</Isp>
				      <Region>591</Region>
				      <Country>629</Country>
				      <City>407</City>
				      <IspName.en>China-Mobile</IspName.en>
				      <IspName.zh_CN>中国移动</IspName.zh_CN>
				      <Region.en>Hubei</Region.en>
				      <Country.en>China</Country.en>
				      <IPV6ProbeCount>0</IPV6ProbeCount>
				      <IPV4ProbeCount>2</IPV4ProbeCount>
				      <CityName.zh_CN>荆州市</CityName.zh_CN>
			    </IspCity>
		  </IspCityList>
		  <Success>true</Success>
		  <Code>200</Code>
</DescribeSiteMonitorISPCityListResponse>
```

`JSON` 格式

```
{
    "Message": "successful",
    "IspCityList": {
        "IspCity": [
           {
				"Country.zh_CN": "中国",
				"CityName.en": "Yantai",
				"Region.zh_CN": "山东省",
				"Isp": "5",
				"Region": "200",
				"Country": "629",
				"City": "428",
				"IspName.en": "China-Mobile",
				"IspName.zh_CN": "中国移动",
				"Region.en": "Shandong",
				"Country.en": "China",
				"IPV6ProbeCount": 0,
				"IPV4ProbeCount": 2,
				"CityName.zh_CN": "烟台市"
			},
			{
				"Country.zh_CN": "中国",
				"CityName.en": "Xian",
				"Region.zh_CN": "陕西省",
				"Isp": "507",
				"Region": "28",
				"Country": "629",
				"City": "311",
				"IspName.en": "DrPeng",
				"IspName.zh_CN": "鹏博士",
				"Region.en": "Shaanxi",
				"Country.en": "China",
				"IPV6ProbeCount": 0,
				"IPV4ProbeCount": 2,
				"CityName.zh_CN": "西安市"
			},
			{
				"Country.zh_CN": "中国",
				"CityName.en": "Jingzhou",
				"Region.zh_CN": "湖北省",
				"Isp": "5",
				"Region": "591",
				"Country": "629",
				"City": "407",
				"IspName.en": "China-Mobile",
				"IspName.zh_CN": "中国移动",
				"Region.en": "Hubei",
				"Country.en": "China",
				"IPV6ProbeCount": 0,
				"IPV4ProbeCount": 2,
				"CityName.zh_CN": "荆州市"
			}
        ]
    },
    "Success": true,
    "Code": "200"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

