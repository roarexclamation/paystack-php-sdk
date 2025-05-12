# OpenAPI\Client\SplitApi

All URIs are relative to https://api.paystack.co, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**splitAddSubaccount()**](SplitApi.md#splitAddSubaccount) | **POST** /split/{id}/subaccount/add | Add Subaccount to Split |
| [**splitCreate()**](SplitApi.md#splitCreate) | **POST** /split | Create Split |
| [**splitFetch()**](SplitApi.md#splitFetch) | **GET** /split/{id} | Fetch Split |
| [**splitList()**](SplitApi.md#splitList) | **GET** /split | List/Search Splits |
| [**splitRemoveSubaccount()**](SplitApi.md#splitRemoveSubaccount) | **POST** /split/{id}/subaccount/remove | Remove Subaccount from split |
| [**splitUpdate()**](SplitApi.md#splitUpdate) | **PUT** /split/{id} | Update Split |


## `splitAddSubaccount()`

```php
splitAddSubaccount($id, $split_subaccounts): \OpenAPI\Client\Model\SplitAddUpdateSubaccountResponse
```

Add Subaccount to Split

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SplitApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = application/json; // string
$split_subaccounts = new \OpenAPI\Client\Model\SplitSubaccounts(); // \OpenAPI\Client\Model\SplitSubaccounts

try {
    $result = $apiInstance->splitAddSubaccount($id, $split_subaccounts);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SplitApi->splitAddSubaccount: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |
| **split_subaccounts** | [**\OpenAPI\Client\Model\SplitSubaccounts**](../Model/SplitSubaccounts.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\SplitAddUpdateSubaccountResponse**](../Model/SplitAddUpdateSubaccountResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `splitCreate()`

```php
splitCreate($split_create): \OpenAPI\Client\Model\SplitCreateResponse
```

Create Split

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SplitApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$split_create = new \OpenAPI\Client\Model\SplitCreate(); // \OpenAPI\Client\Model\SplitCreate

try {
    $result = $apiInstance->splitCreate($split_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SplitApi->splitCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **split_create** | [**\OpenAPI\Client\Model\SplitCreate**](../Model/SplitCreate.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\SplitCreateResponse**](../Model/SplitCreateResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `splitFetch()`

```php
splitFetch($id): \OpenAPI\Client\Model\SplitFetchResponse
```

Fetch Split

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SplitApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $result = $apiInstance->splitFetch($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SplitApi->splitFetch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\SplitFetchResponse**](../Model/SplitFetchResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `splitList()`

```php
splitList($name, $active, $sort_by, $from, $to, $per_page, $page): \OpenAPI\Client\Model\SplitListResponse
```

List/Search Splits

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SplitApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$name = 'name_example'; // string
$active = 'active_example'; // string
$sort_by = 'sort_by_example'; // string
$from = 'from_example'; // string
$to = 'to_example'; // string
$per_page = 'per_page_example'; // string
$page = 'page_example'; // string

try {
    $result = $apiInstance->splitList($name, $active, $sort_by, $from, $to, $per_page, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SplitApi->splitList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **name** | **string**|  | [optional] |
| **active** | **string**|  | [optional] |
| **sort_by** | **string**|  | [optional] |
| **from** | **string**|  | [optional] |
| **to** | **string**|  | [optional] |
| **per_page** | **string**|  | [optional] |
| **page** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\SplitListResponse**](../Model/SplitListResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `splitRemoveSubaccount()`

```php
splitRemoveSubaccount($id, $split_subaccounts): \OpenAPI\Client\Model\SplitRemoveSubaccountResponse
```

Remove Subaccount from split

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SplitApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$split_subaccounts = new \OpenAPI\Client\Model\SplitSubaccounts(); // \OpenAPI\Client\Model\SplitSubaccounts

try {
    $result = $apiInstance->splitRemoveSubaccount($id, $split_subaccounts);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SplitApi->splitRemoveSubaccount: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |
| **split_subaccounts** | [**\OpenAPI\Client\Model\SplitSubaccounts**](../Model/SplitSubaccounts.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\SplitRemoveSubaccountResponse**](../Model/SplitRemoveSubaccountResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `splitUpdate()`

```php
splitUpdate($id, $split_update): \OpenAPI\Client\Model\SplitUpdateResponse
```

Update Split

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SplitApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$split_update = new \OpenAPI\Client\Model\SplitUpdate(); // \OpenAPI\Client\Model\SplitUpdate

try {
    $result = $apiInstance->splitUpdate($id, $split_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SplitApi->splitUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |
| **split_update** | [**\OpenAPI\Client\Model\SplitUpdate**](../Model/SplitUpdate.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\SplitUpdateResponse**](../Model/SplitUpdateResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
