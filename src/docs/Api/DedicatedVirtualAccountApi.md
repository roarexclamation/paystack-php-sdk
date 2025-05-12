# OpenAPI\Client\DedicatedVirtualAccountApi

All URIs are relative to https://api.paystack.co, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**dedicatedAccountAddSplit()**](DedicatedVirtualAccountApi.md#dedicatedAccountAddSplit) | **POST** /dedicated_account/split | Split Dedicated Account Transaction |
| [**dedicatedAccountAssign()**](DedicatedVirtualAccountApi.md#dedicatedAccountAssign) | **POST** /dedicated_account/assign | Assign Dedicated Account |
| [**dedicatedAccountAvailableProviders()**](DedicatedVirtualAccountApi.md#dedicatedAccountAvailableProviders) | **GET** /dedicated_account/available_providers | Fetch Bank Providers |
| [**dedicatedAccountCreate()**](DedicatedVirtualAccountApi.md#dedicatedAccountCreate) | **POST** /dedicated_account | Create Dedicated Account |
| [**dedicatedAccountDeactivate()**](DedicatedVirtualAccountApi.md#dedicatedAccountDeactivate) | **DELETE** /dedicated_account/{account_id} | Deactivate Dedicated Account |
| [**dedicatedAccountFetch()**](DedicatedVirtualAccountApi.md#dedicatedAccountFetch) | **GET** /dedicated_account/{account_id} | Fetch Dedicated Account |
| [**dedicatedAccountList()**](DedicatedVirtualAccountApi.md#dedicatedAccountList) | **GET** /dedicated_account | List Dedicated Accounts |
| [**dedicatedAccountRemoveSplit()**](DedicatedVirtualAccountApi.md#dedicatedAccountRemoveSplit) | **DELETE** /dedicated_account/split | Remove Split from Dedicated Account |
| [**dedicatedAccountRequery()**](DedicatedVirtualAccountApi.md#dedicatedAccountRequery) | **GET** /dedicated_account/requery | Requery Dedicated Account |


## `dedicatedAccountAddSplit()`

```php
dedicatedAccountAddSplit($dedicated_virtual_account_split): \OpenAPI\Client\Model\Response
```

Split Dedicated Account Transaction

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DedicatedVirtualAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$dedicated_virtual_account_split = new \OpenAPI\Client\Model\DedicatedVirtualAccountSplit(); // \OpenAPI\Client\Model\DedicatedVirtualAccountSplit

try {
    $result = $apiInstance->dedicatedAccountAddSplit($dedicated_virtual_account_split);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DedicatedVirtualAccountApi->dedicatedAccountAddSplit: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **dedicated_virtual_account_split** | [**\OpenAPI\Client\Model\DedicatedVirtualAccountSplit**](../Model/DedicatedVirtualAccountSplit.md)|  | [optional] |

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

## `dedicatedAccountAssign()`

```php
dedicatedAccountAssign($dedicated_virtual_account_assign): \OpenAPI\Client\Model\Response
```

Assign Dedicated Account

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DedicatedVirtualAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$dedicated_virtual_account_assign = new \OpenAPI\Client\Model\DedicatedVirtualAccountAssign(); // \OpenAPI\Client\Model\DedicatedVirtualAccountAssign

try {
    $result = $apiInstance->dedicatedAccountAssign($dedicated_virtual_account_assign);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DedicatedVirtualAccountApi->dedicatedAccountAssign: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **dedicated_virtual_account_assign** | [**\OpenAPI\Client\Model\DedicatedVirtualAccountAssign**](../Model/DedicatedVirtualAccountAssign.md)|  | [optional] |

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

## `dedicatedAccountAvailableProviders()`

```php
dedicatedAccountAvailableProviders(): \OpenAPI\Client\Model\Response
```

Fetch Bank Providers

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DedicatedVirtualAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->dedicatedAccountAvailableProviders();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DedicatedVirtualAccountApi->dedicatedAccountAvailableProviders: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

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

## `dedicatedAccountCreate()`

```php
dedicatedAccountCreate($dedicated_virtual_account_create): \OpenAPI\Client\Model\DedicatedNubanCreateResponse
```

Create Dedicated Account

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DedicatedVirtualAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$dedicated_virtual_account_create = new \OpenAPI\Client\Model\DedicatedVirtualAccountCreate(); // \OpenAPI\Client\Model\DedicatedVirtualAccountCreate

try {
    $result = $apiInstance->dedicatedAccountCreate($dedicated_virtual_account_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DedicatedVirtualAccountApi->dedicatedAccountCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **dedicated_virtual_account_create** | [**\OpenAPI\Client\Model\DedicatedVirtualAccountCreate**](../Model/DedicatedVirtualAccountCreate.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\DedicatedNubanCreateResponse**](../Model/DedicatedNubanCreateResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `dedicatedAccountDeactivate()`

```php
dedicatedAccountDeactivate($account_id): \OpenAPI\Client\Model\DedicatedNubanDeactivateResponse
```

Deactivate Dedicated Account

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DedicatedVirtualAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string

try {
    $result = $apiInstance->dedicatedAccountDeactivate($account_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DedicatedVirtualAccountApi->dedicatedAccountDeactivate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\DedicatedNubanDeactivateResponse**](../Model/DedicatedNubanDeactivateResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `dedicatedAccountFetch()`

```php
dedicatedAccountFetch($account_id): \OpenAPI\Client\Model\DedicatedNubanFetchResponse
```

Fetch Dedicated Account

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DedicatedVirtualAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string

try {
    $result = $apiInstance->dedicatedAccountFetch($account_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DedicatedVirtualAccountApi->dedicatedAccountFetch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\DedicatedNubanFetchResponse**](../Model/DedicatedNubanFetchResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `dedicatedAccountList()`

```php
dedicatedAccountList($account_number, $customer, $active, $currency, $provider_slug, $bank_id, $per_page, $page): \OpenAPI\Client\Model\DedicatedNubanFetchResponse
```

List Dedicated Accounts

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DedicatedVirtualAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_number = 'account_number_example'; // string
$customer = 'customer_example'; // string
$active = True; // bool
$currency = 'currency_example'; // string
$provider_slug = 'provider_slug_example'; // string
$bank_id = 'bank_id_example'; // string
$per_page = 'per_page_example'; // string
$page = 'page_example'; // string

try {
    $result = $apiInstance->dedicatedAccountList($account_number, $customer, $active, $currency, $provider_slug, $bank_id, $per_page, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DedicatedVirtualAccountApi->dedicatedAccountList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_number** | **string**|  | [optional] |
| **customer** | **string**|  | [optional] |
| **active** | **bool**|  | [optional] |
| **currency** | **string**|  | [optional] |
| **provider_slug** | **string**|  | [optional] |
| **bank_id** | **string**|  | [optional] |
| **per_page** | **string**|  | [optional] |
| **page** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\DedicatedNubanFetchResponse**](../Model/DedicatedNubanFetchResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `dedicatedAccountRemoveSplit()`

```php
dedicatedAccountRemoveSplit($dedicated_virtual_account_split): \OpenAPI\Client\Model\Response
```

Remove Split from Dedicated Account

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DedicatedVirtualAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$dedicated_virtual_account_split = new \OpenAPI\Client\Model\DedicatedVirtualAccountSplit(); // \OpenAPI\Client\Model\DedicatedVirtualAccountSplit

try {
    $result = $apiInstance->dedicatedAccountRemoveSplit($dedicated_virtual_account_split);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DedicatedVirtualAccountApi->dedicatedAccountRemoveSplit: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **dedicated_virtual_account_split** | [**\OpenAPI\Client\Model\DedicatedVirtualAccountSplit**](../Model/DedicatedVirtualAccountSplit.md)|  | [optional] |

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

## `dedicatedAccountRequery()`

```php
dedicatedAccountRequery($account_number, $provider_slug, $date): \OpenAPI\Client\Model\Response
```

Requery Dedicated Account

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DedicatedVirtualAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_number = 'account_number_example'; // string | Virtual account number to requery
$provider_slug = 'provider_slug_example'; // string | The bank's slug in lowercase, without spaces e.g. `wema-bank`
$date = 'date_example'; // string | The day the transfer was made in `YYYY-MM-DD` format

try {
    $result = $apiInstance->dedicatedAccountRequery($account_number, $provider_slug, $date);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DedicatedVirtualAccountApi->dedicatedAccountRequery: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_number** | **string**| Virtual account number to requery | [optional] |
| **provider_slug** | **string**| The bank&#39;s slug in lowercase, without spaces e.g. &#x60;wema-bank&#x60; | [optional] |
| **date** | **string**| The day the transfer was made in &#x60;YYYY-MM-DD&#x60; format | [optional] |

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
