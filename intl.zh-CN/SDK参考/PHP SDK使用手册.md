# PHP SDK使用手册 {#concept_qhh_zbp_zdb .concept}

## SDK下载 {#section_fb2_1cp_zdb .section}

Github下载地址：

-   [https://github.com/aliyun/aliyun-openapi-php-sdk/tree/master/aliyun-php-sdk-cms/](https://github.com/aliyun/aliyun-openapi-php-sdk/tree/master/aliyun-php-sdk-cms/)
-   [https://github.com/aliyun/aliyun-openapi-php-sdk/tree/master/aliyun-php-sdk-core](https://github.com/aliyun/aliyun-openapi-php-sdk/tree/master/aliyun-php-sdk-core)

## 测试代码 {#section_qtx_1cp_zdb .section}

```
<?php
use AlibabaCloud\Client\AlibabaCloud;
use AlibabaCloud\Client\Exception\ClientException;
use AlibabaCloud\Client\Exception\ServerException;

// Download：https://github.com/aliyun/openapi-sdk-php
// Usage：https://github.com/aliyun/openapi-sdk-php/blob/master/README.md

AlibabaCloud::accessKeyClient('<accessKeyId>', '<accessSecret>')
                        ->regionId('cn-beijing')
                        ->asDefaultClient();

try {
    $result = AlibabaCloud::rpc()
                          ->product('Cms')
                          // ->scheme('https') // https | http
                          ->version('2019-01-01')
                          ->action('DescribeMetricList')
                          ->method('POST')
                          ->options([
                                        'query' => [
                                          'RegionId' => 'cn-beijing',
                                          'MetricName' => 'cpu_idle',
                                          'Namespace' => 'acs_ecs_dashboard',
                                          'Period' => '60',
                                          'StartTime' => '2019-05-13 10:20:27',
                                          'EndTime' => '2019-05-13 11:06:27',
                                          'Dimensions' => '{\"instanceId\":<instanceId_as_example>}',
                                        ],
                                    ])
                          ->request();
    print_r($result->toArray());
} catch (ClientException $e) {
    echo $e->getErrorMessage() . PHP_EOL;
} catch (ServerException $e) {
    echo $e->getErrorMessage() . PHP_EOL;
}
```

