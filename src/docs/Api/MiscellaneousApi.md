# OpenAPI\Client\MiscellaneousApi

All URIs are relative to https://api.paystack.co, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**miscellaneousAvs()**](MiscellaneousApi.md#miscellaneousAvs) | **GET** /address_verification/states | List States (AVS) |
| [**miscellaneousListCountries()**](MiscellaneousApi.md#miscellaneousListCountries) | **GET** /country | List Countries |
| [**miscellaneousResolveCardBin()**](MiscellaneousApi.md#miscellaneousResolveCardBin) | **GET** /decision/bin/{bin} | Resolve Card BIN |


## `miscellaneousAvs()`

```php
miscellaneousAvs($type, $country, $currency): \OpenAPI\Client\Model\MiscellaneousListStatesResponse
```

List States (AVS)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\MiscellaneousApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$type = 'type_example'; // string
$country = 'country_example'; // string
$currency = 'currency_example'; // string

try {
    $result = $apiInstance->miscellaneousAvs($type, $country, $currency);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MiscellaneousApi->miscellaneousAvs: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **type** | **string**|  | [optional] |
| **country** | **string**|  | [optional] |
| **currency** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\MiscellaneousListStatesResponse**](../Model/MiscellaneousListStatesResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `miscellaneousListCountries()`

```php
miscellaneousListCountries(): \OpenAPI\Client\Model\MiscellaneousListCountriesResponse
```

List Countries

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\MiscellaneousApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->miscellaneousListCountries();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MiscellaneousApi->miscellaneousListCountries: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\MiscellaneousListCountriesResponse**](../Model/MiscellaneousListCountriesResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `miscellaneousResolveCardBin()`

```php
miscellaneousResolveCardBin($bin): \OpenAPI\Client\Model\VerificationResolveCardBINResponse
```

Resolve Card BIN

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\MiscellaneousApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$bin = 'bin_example'; // string

try {
    $result = $apiInstance->miscellaneousResolveCardBin($bin);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MiscellaneousApi->miscellaneousResolveCardBin: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **bin** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\VerificationResolveCardBINResponse**](../Model/VerificationResolveCardBINResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
