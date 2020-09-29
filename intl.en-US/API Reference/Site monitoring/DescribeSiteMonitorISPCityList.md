# DescribeSiteMonitorISPCityList

Queries the detection points that are available for creating site monitoring tasks.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeSiteMonitorISPCityList&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeSiteMonitorISPCityList|The operation that you want to perform. Set the value to DescribeSiteMonitorISPCityList. |
|Isp|String|No|China Mobile|The name or ID of the carrier to which the detection point belongs. Fuzzy search is supported for carrier names. |
|City|String|No|Beijing|The name or ID of the city where the detection point resides. Fuzzy search is supported for city names. |
|IPV6|Boolean|No|false|Specifies whether to query the detection points that use IPv6. Valid values:

-   true
-   false |
|IPV4|Boolean|No|true|Specifies whether to query the detection points that use IPv4. Valid values:

-   true
-   false |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|RequestId|String|848EF34A-FD9F-48A6-879F-414279ED4F26|The ID of the request. |
|Message|String|successful|The returned message. |
|IspCityList|Array of IspCity|N/A|The detection points that were found. |
|IspCity|N/A|N/A|N/A|
|City|String|738|The ID of a city. |
|CityName.en|String|Yantai|The name of the city. |
|Country.en|String|China|The name of the country. |
|IPV4ProbeCount|String|2|The number of detection points that use IPv4. |
|IPV6ProbeCount|String|3|The number of detection points that use IPv6. |
|Isp|String|232|The ID of the carrier. |
|IspName.en|String|China-Mobile|The name of the carrier. |
|Region|String|200|The code of the province. |
|Region.en|String|Shandong|The name of the province. |
|Success|String|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=DescribeSiteMonitorISPCityList
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeSiteMonitorISPCityListResponse>
          <Message>successful</Message>
                <IspCity>
                      <Country.zh_CN>China</Country.zh_CN>
                      <CityName.en>Xian</CityName.en>
                      <Region.zh_CN>Shaanxi</Region.zh_CN>
                      <Isp>507</Isp>
                      <Region>28</Region>
                      <Country>629</Country>
                      <City>311</City>
                      <IspName.en>DrPeng</IspName.en>
                      <IspName.zh_CN>Dr.Peng</IspName.zh_CN>
                      <Region.en>Shaanxi</Region.en>
                      <Country.en>China</Country.en>
                      <IPV6ProbeCount>0</IPV6ProbeCount>
                      <IPV4ProbeCount>2</IPV4ProbeCount>
                      <CityName.zh_CN>Xi'an</CityName.zh_CN>
                </IspCity>
                <IspCity>
                      <Country.zh_CN>China</Country.zh_CN>
                      <CityName.en>Jingzhou</CityName.en>
                      <Region.zh_CN>Hubei</Region.zh_CN>
                      <Isp>5</Isp>
                      <Region>591</Region>
                      <Country>629</Country>
                      <City>407</City>
                      <IspName.en>China-Mobile</IspName.en>
                      <IspName.zh_CN>China Mobile</IspName.zh_CN>
                      <Region.en>Hubei</Region.en>
                      <Country.en>China</Country.en>
                      <IPV6ProbeCount>0</IPV6ProbeCount>
                      <IPV4ProbeCount>2</IPV4ProbeCount>
                      <CityName.zh_CN>Jingzhou</CityName.zh_CN>
                </IspCity>
          </IspCityList>
          <Success>true</Success>
          <Code>200</Code>
</DescribeSiteMonitorISPCityListResponse>
```

`JSON` format

```
{
    "Message": "successful",
    "IspCityList": {
        "IspCity": [
            {
                "Country.zh_CN": "China",
                "CityName.en": "Xian",
                "Region.zh_CN": "Shaanxi",
                "Isp": "507",
                "Region": "28",
                "Country": "629",
                "City": "311",
                "IspName.en": "DrPeng",
                "IspName.zh_CN": "Dr.Peng",
                "Region.en": "Shaanxi",
                "Country.en": "China",
                "IPV6ProbeCount": 0,
                "IPV4ProbeCount": 2,
                "CityName.zh_CN": "Xi'an"
            },
            {
                "Country.zh_CN": "China",
                "CityName.en": "Jingzhou",
                "Region.zh_CN": "Hubei",
                "Isp": "5",
                "Region": "591",
                "Country": "629",
                "City": "407",
                "IspName.en": "China-Mobile",
                "IspName.zh_CN": "China Mobile",
                "Region.en": "Hubei",
                "Country.en": "China",
                "IPV6ProbeCount": 0,
                "IPV4ProbeCount": 2,
                "CityName.zh_CN": "Jingzhou"
            }
        ]
    },
    "Success": true,
    "Code": "200"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

