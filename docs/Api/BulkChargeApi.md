# OpenAPI\Client\BulkChargeApi

All URIs are relative to https://api.paystack.co, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**bulkChargeCharges()**](BulkChargeApi.md#bulkChargeCharges) | **GET** /bulkcharge/{code}/charges | Fetch Charges in a Batch |
| [**bulkChargeFetch()**](BulkChargeApi.md#bulkChargeFetch) | **GET** /bulkcharge/{code} | Fetch Bulk Charge Batch |
| [**bulkChargeInitiate()**](BulkChargeApi.md#bulkChargeInitiate) | **POST** /bulkcharge | Initiate Bulk Charge |
| [**bulkChargeList()**](BulkChargeApi.md#bulkChargeList) | **GET** /bulkcharge | List Bulk Charge Batches |
| [**bulkChargePause()**](BulkChargeApi.md#bulkChargePause) | **GET** /bulkcharge/pause/{code} | Pause Bulk Charge Batch |
| [**bulkChargeResume()**](BulkChargeApi.md#bulkChargeResume) | **GET** /bulkcharge/resume/{code} | Resume Bulk Charge Batch |


## `bulkChargeCharges()`

```php
bulkChargeCharges($code): \OpenAPI\Client\Model\BulkChargeFetchBulkBatchChargesResponse
```

Fetch Charges in a Batch

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BulkChargeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$code = 'code_example'; // string | Batch code

try {
    $result = $apiInstance->bulkChargeCharges($code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BulkChargeApi->bulkChargeCharges: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**| Batch code | |

### Return type

[**\OpenAPI\Client\Model\BulkChargeFetchBulkBatchChargesResponse**](../Model/BulkChargeFetchBulkBatchChargesResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `bulkChargeFetch()`

```php
bulkChargeFetch($code): \OpenAPI\Client\Model\BulkChargeFetchResponse
```

Fetch Bulk Charge Batch

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BulkChargeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$code = 'code_example'; // string | Batch code

try {
    $result = $apiInstance->bulkChargeFetch($code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BulkChargeApi->bulkChargeFetch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**| Batch code | |

### Return type

[**\OpenAPI\Client\Model\BulkChargeFetchResponse**](../Model/BulkChargeFetchResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `bulkChargeInitiate()`

```php
bulkChargeInitiate($bulk_charge_initiate_request_inner): \OpenAPI\Client\Model\BulkChargeInitiateResponse
```

Initiate Bulk Charge

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BulkChargeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$bulk_charge_initiate_request_inner = array(new \OpenAPI\Client\Model\BulkChargeInitiateRequestInner()); // \OpenAPI\Client\Model\BulkChargeInitiateRequestInner[]

try {
    $result = $apiInstance->bulkChargeInitiate($bulk_charge_initiate_request_inner);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BulkChargeApi->bulkChargeInitiate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **bulk_charge_initiate_request_inner** | [**\OpenAPI\Client\Model\BulkChargeInitiateRequestInner[]**](../Model/BulkChargeInitiateRequestInner.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\BulkChargeInitiateResponse**](../Model/BulkChargeInitiateResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `bulkChargeList()`

```php
bulkChargeList($per_page, $page, $from, $to): \OpenAPI\Client\Model\BulkChargeListResponse
```

List Bulk Charge Batches

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BulkChargeApi(
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
    $result = $apiInstance->bulkChargeList($per_page, $page, $from, $to);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BulkChargeApi->bulkChargeList: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\BulkChargeListResponse**](../Model/BulkChargeListResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `bulkChargePause()`

```php
bulkChargePause($code): \OpenAPI\Client\Model\BulkChargePauseResponse
```

Pause Bulk Charge Batch

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BulkChargeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$code = 'code_example'; // string | Batch code

try {
    $result = $apiInstance->bulkChargePause($code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BulkChargeApi->bulkChargePause: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**| Batch code | |

### Return type

[**\OpenAPI\Client\Model\BulkChargePauseResponse**](../Model/BulkChargePauseResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `bulkChargeResume()`

```php
bulkChargeResume($code): \OpenAPI\Client\Model\BulkChargeResumeResponse
```

Resume Bulk Charge Batch

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BulkChargeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$code = 'code_example'; // string | Batch code

try {
    $result = $apiInstance->bulkChargeResume($code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BulkChargeApi->bulkChargeResume: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**| Batch code | |

### Return type

[**\OpenAPI\Client\Model\BulkChargeResumeResponse**](../Model/BulkChargeResumeResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
