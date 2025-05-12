# OpenAPI\Client\TransferRecipientApi

All URIs are relative to https://api.paystack.co, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**transferrecipientBulk()**](TransferRecipientApi.md#transferrecipientBulk) | **POST** /transferrecipient/bulk | Bulk Create Transfer Recipient |
| [**transferrecipientCreate()**](TransferRecipientApi.md#transferrecipientCreate) | **POST** /transferrecipient | Create Transfer Recipient |
| [**transferrecipientDelete()**](TransferRecipientApi.md#transferrecipientDelete) | **DELETE** /transferrecipient/{code} | Delete Transfer Recipient |
| [**transferrecipientFetch()**](TransferRecipientApi.md#transferrecipientFetch) | **GET** /transferrecipient/{code} | Fetch Transfer recipient |
| [**transferrecipientList()**](TransferRecipientApi.md#transferrecipientList) | **GET** /transferrecipient | List Transfer Recipients |
| [**transferrecipientUpdate()**](TransferRecipientApi.md#transferrecipientUpdate) | **PUT** /transferrecipient/{code} | Update Transfer recipient |


## `transferrecipientBulk()`

```php
transferrecipientBulk($transfer_recipient_bulk): \OpenAPI\Client\Model\TransferRecipientBulkCreateResponse
```

Bulk Create Transfer Recipient

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TransferRecipientApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$transfer_recipient_bulk = new \OpenAPI\Client\Model\TransferRecipientBulk(); // \OpenAPI\Client\Model\TransferRecipientBulk

try {
    $result = $apiInstance->transferrecipientBulk($transfer_recipient_bulk);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransferRecipientApi->transferrecipientBulk: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **transfer_recipient_bulk** | [**\OpenAPI\Client\Model\TransferRecipientBulk**](../Model/TransferRecipientBulk.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\TransferRecipientBulkCreateResponse**](../Model/TransferRecipientBulkCreateResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `transferrecipientCreate()`

```php
transferrecipientCreate($transfer_recipient_create): \OpenAPI\Client\Model\TransferRecipientCreateResponse
```

Create Transfer Recipient

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TransferRecipientApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$transfer_recipient_create = new \OpenAPI\Client\Model\TransferRecipientCreate(); // \OpenAPI\Client\Model\TransferRecipientCreate

try {
    $result = $apiInstance->transferrecipientCreate($transfer_recipient_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransferRecipientApi->transferrecipientCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **transfer_recipient_create** | [**\OpenAPI\Client\Model\TransferRecipientCreate**](../Model/TransferRecipientCreate.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\TransferRecipientCreateResponse**](../Model/TransferRecipientCreateResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `transferrecipientDelete()`

```php
transferrecipientDelete($code): \OpenAPI\Client\Model\TransferRecipientDeleteResponse
```

Delete Transfer Recipient

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TransferRecipientApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$code = 'code_example'; // string | Transfer recipient code

try {
    $result = $apiInstance->transferrecipientDelete($code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransferRecipientApi->transferrecipientDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**| Transfer recipient code | |

### Return type

[**\OpenAPI\Client\Model\TransferRecipientDeleteResponse**](../Model/TransferRecipientDeleteResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `transferrecipientFetch()`

```php
transferrecipientFetch($code): \OpenAPI\Client\Model\TransferRecipientFetchResponse
```

Fetch Transfer recipient

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TransferRecipientApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$code = 'code_example'; // string | Transfer recipient code

try {
    $result = $apiInstance->transferrecipientFetch($code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransferRecipientApi->transferrecipientFetch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**| Transfer recipient code | |

### Return type

[**\OpenAPI\Client\Model\TransferRecipientFetchResponse**](../Model/TransferRecipientFetchResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `transferrecipientList()`

```php
transferrecipientList($per_page, $page, $from, $to): \OpenAPI\Client\Model\TransferRecipientListResponse
```

List Transfer Recipients

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TransferRecipientApi(
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
    $result = $apiInstance->transferrecipientList($per_page, $page, $from, $to);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransferRecipientApi->transferrecipientList: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\TransferRecipientListResponse**](../Model/TransferRecipientListResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `transferrecipientUpdate()`

```php
transferrecipientUpdate($code, $transfer_recipient_update): \OpenAPI\Client\Model\TransferRecipientUpdateResponse
```

Update Transfer recipient

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TransferRecipientApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$code = 'code_example'; // string | Transfer recipient code
$transfer_recipient_update = new \OpenAPI\Client\Model\TransferRecipientUpdate(); // \OpenAPI\Client\Model\TransferRecipientUpdate

try {
    $result = $apiInstance->transferrecipientUpdate($code, $transfer_recipient_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransferRecipientApi->transferrecipientUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**| Transfer recipient code | |
| **transfer_recipient_update** | [**\OpenAPI\Client\Model\TransferRecipientUpdate**](../Model/TransferRecipientUpdate.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\TransferRecipientUpdateResponse**](../Model/TransferRecipientUpdateResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
