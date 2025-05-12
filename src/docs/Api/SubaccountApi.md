# OpenAPI\Client\SubaccountApi

All URIs are relative to https://api.paystack.co, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**subaccountCreate()**](SubaccountApi.md#subaccountCreate) | **POST** /subaccount | Create Subaccount |
| [**subaccountFetch()**](SubaccountApi.md#subaccountFetch) | **GET** /subaccount/{code} | Fetch Subaccount |
| [**subaccountList()**](SubaccountApi.md#subaccountList) | **GET** /subaccount | List Subaccounts |
| [**subaccountUpdate()**](SubaccountApi.md#subaccountUpdate) | **PUT** /subaccount/{code} | Update Subaccount |


## `subaccountCreate()`

```php
subaccountCreate($subaccount_create): \OpenAPI\Client\Model\SubaccountCreateResponse
```

Create Subaccount

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SubaccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$subaccount_create = new \OpenAPI\Client\Model\SubaccountCreate(); // \OpenAPI\Client\Model\SubaccountCreate

try {
    $result = $apiInstance->subaccountCreate($subaccount_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubaccountApi->subaccountCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **subaccount_create** | [**\OpenAPI\Client\Model\SubaccountCreate**](../Model/SubaccountCreate.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\SubaccountCreateResponse**](../Model/SubaccountCreateResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `subaccountFetch()`

```php
subaccountFetch($code): \OpenAPI\Client\Model\SubaccountFetchResponse
```

Fetch Subaccount

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SubaccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$code = 'code_example'; // string

try {
    $result = $apiInstance->subaccountFetch($code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubaccountApi->subaccountFetch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\SubaccountFetchResponse**](../Model/SubaccountFetchResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `subaccountList()`

```php
subaccountList($per_page, $page, $from, $to): \OpenAPI\Client\Model\SubaccountListResponse
```

List Subaccounts

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SubaccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$per_page = 56; // int | Number of records to fetch per page
$page = 56; // int | The section to retrieve
$from = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | The start date
$to = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | The end date

try {
    $result = $apiInstance->subaccountList($per_page, $page, $from, $to);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubaccountApi->subaccountList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **per_page** | **int**| Number of records to fetch per page | [optional] |
| **page** | **int**| The section to retrieve | [optional] |
| **from** | **\DateTime**| The start date | [optional] |
| **to** | **\DateTime**| The end date | [optional] |

### Return type

[**\OpenAPI\Client\Model\SubaccountListResponse**](../Model/SubaccountListResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `subaccountUpdate()`

```php
subaccountUpdate($code, $subaccount_update): \OpenAPI\Client\Model\SubaccountUpdateResponse
```

Update Subaccount

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SubaccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$code = 'code_example'; // string
$subaccount_update = new \OpenAPI\Client\Model\SubaccountUpdate(); // \OpenAPI\Client\Model\SubaccountUpdate

try {
    $result = $apiInstance->subaccountUpdate($code, $subaccount_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubaccountApi->subaccountUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**|  | |
| **subaccount_update** | [**\OpenAPI\Client\Model\SubaccountUpdate**](../Model/SubaccountUpdate.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\SubaccountUpdateResponse**](../Model/SubaccountUpdateResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
