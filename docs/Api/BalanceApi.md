# OpenAPI\Client\BalanceApi

All URIs are relative to https://api.paystack.co, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**balanceFetch()**](BalanceApi.md#balanceFetch) | **GET** /balance | Fetch Balance |
| [**balanceLedger()**](BalanceApi.md#balanceLedger) | **GET** /balance/ledger | Balance Ledger |


## `balanceFetch()`

```php
balanceFetch(): \OpenAPI\Client\Model\BalanceCheckResponse
```

Fetch Balance

You can only transfer from what you have

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BalanceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->balanceFetch();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BalanceApi->balanceFetch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\BalanceCheckResponse**](../Model/BalanceCheckResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `balanceLedger()`

```php
balanceLedger($per_page, $page, $from, $to): \OpenAPI\Client\Model\BalanceFetchLedgerResponse
```

Balance Ledger

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BalanceApi(
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
    $result = $apiInstance->balanceLedger($per_page, $page, $from, $to);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BalanceApi->balanceLedger: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\BalanceFetchLedgerResponse**](../Model/BalanceFetchLedgerResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
