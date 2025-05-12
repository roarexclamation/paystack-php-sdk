# OpenAPI\Client\ApplePayApi

All URIs are relative to https://api.paystack.co, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**applePayListDomain()**](ApplePayApi.md#applePayListDomain) | **GET** /apple-pay/domain | List Domains |
| [**applePayRegisterDomain()**](ApplePayApi.md#applePayRegisterDomain) | **POST** /apple-pay/domain | Register Domain |
| [**applePayUnregisterDomain()**](ApplePayApi.md#applePayUnregisterDomain) | **DELETE** /apple-pay/domain | Unregister Domain |


## `applePayListDomain()`

```php
applePayListDomain($use_cursor, $next, $previous): \OpenAPI\Client\Model\Response
```

List Domains

Lists all registered domains on your integration

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ApplePayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$use_cursor = True; // bool
$next = 'next_example'; // string
$previous = 'previous_example'; // string

try {
    $result = $apiInstance->applePayListDomain($use_cursor, $next, $previous);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplePayApi->applePayListDomain: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **use_cursor** | **bool**|  | [optional] |
| **next** | **string**|  | [optional] |
| **previous** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\Response**](../Model/Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `applePayRegisterDomain()`

```php
applePayRegisterDomain($apple_pay_param): \OpenAPI\Client\Model\ApplePayCreateOkModel
```

Register Domain

Register a top-level domain or subdomain for your Apple Pay integration.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ApplePayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$apple_pay_param = new \OpenAPI\Client\Model\ApplePayParam(); // \OpenAPI\Client\Model\ApplePayParam

try {
    $result = $apiInstance->applePayRegisterDomain($apple_pay_param);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplePayApi->applePayRegisterDomain: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **apple_pay_param** | [**\OpenAPI\Client\Model\ApplePayParam**](../Model/ApplePayParam.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ApplePayCreateOkModel**](../Model/ApplePayCreateOkModel.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `applePayUnregisterDomain()`

```php
applePayUnregisterDomain($apple_pay_param): \OpenAPI\Client\Model\Response
```

Unregister Domain

Unregister a top-level domain or subdomain previously used for your Apple Pay integration.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ApplePayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$apple_pay_param = new \OpenAPI\Client\Model\ApplePayParam(); // \OpenAPI\Client\Model\ApplePayParam

try {
    $result = $apiInstance->applePayUnregisterDomain($apple_pay_param);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplePayApi->applePayUnregisterDomain: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **apple_pay_param** | [**\OpenAPI\Client\Model\ApplePayParam**](../Model/ApplePayParam.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\Response**](../Model/Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
