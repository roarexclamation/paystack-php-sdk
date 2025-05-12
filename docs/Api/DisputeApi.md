# OpenAPI\Client\DisputeApi

All URIs are relative to https://api.paystack.co, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**disputeDownload()**](DisputeApi.md#disputeDownload) | **GET** /dispute/export | Export Disputes |
| [**disputeEvidence()**](DisputeApi.md#disputeEvidence) | **POST** /dispute/{id}/evidence | Add Evidence |
| [**disputeFetch()**](DisputeApi.md#disputeFetch) | **GET** /dispute/{id} | Fetch Dispute |
| [**disputeList()**](DisputeApi.md#disputeList) | **GET** /dispute | List Disputes |
| [**disputeResolve()**](DisputeApi.md#disputeResolve) | **PUT** /dispute/{id}/resolve | Resolve a Dispute |
| [**disputeTransaction()**](DisputeApi.md#disputeTransaction) | **GET** /dispute/transaction/{id} | List Transaction Disputes |
| [**disputeUpdate()**](DisputeApi.md#disputeUpdate) | **PUT** /dispute/{id} | Update Dispute |
| [**disputeUploadUrl()**](DisputeApi.md#disputeUploadUrl) | **GET** /dispute/{id}/upload_url | Get Upload URL |


## `disputeDownload()`

```php
disputeDownload($per_page, $page, $status, $from, $to): \OpenAPI\Client\Model\DisputeExportResponse
```

Export Disputes

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DisputeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$per_page = 56; // int | Number of records to fetch per page
$page = 56; // int | The section to retrieve
$status = 'status_example'; // string
$from = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | The start date
$to = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | The end date

try {
    $result = $apiInstance->disputeDownload($per_page, $page, $status, $from, $to);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DisputeApi->disputeDownload: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **per_page** | **int**| Number of records to fetch per page | [optional] |
| **page** | **int**| The section to retrieve | [optional] |
| **status** | **string**|  | [optional] |
| **from** | **\DateTime**| The start date | [optional] |
| **to** | **\DateTime**| The end date | [optional] |

### Return type

[**\OpenAPI\Client\Model\DisputeExportResponse**](../Model/DisputeExportResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `disputeEvidence()`

```php
disputeEvidence($id, $dispute_evidence): \OpenAPI\Client\Model\DisputeAddEvidenceResponse
```

Add Evidence

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DisputeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Dispute ID
$dispute_evidence = new \OpenAPI\Client\Model\DisputeEvidence(); // \OpenAPI\Client\Model\DisputeEvidence

try {
    $result = $apiInstance->disputeEvidence($id, $dispute_evidence);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DisputeApi->disputeEvidence: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Dispute ID | |
| **dispute_evidence** | [**\OpenAPI\Client\Model\DisputeEvidence**](../Model/DisputeEvidence.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\DisputeAddEvidenceResponse**](../Model/DisputeAddEvidenceResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `disputeFetch()`

```php
disputeFetch($id): \OpenAPI\Client\Model\DisputeFetchResponse
```

Fetch Dispute

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DisputeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Dispute ID

try {
    $result = $apiInstance->disputeFetch($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DisputeApi->disputeFetch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Dispute ID | |

### Return type

[**\OpenAPI\Client\Model\DisputeFetchResponse**](../Model/DisputeFetchResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `disputeList()`

```php
disputeList($per_page, $page, $status, $transaction, $from, $to): \OpenAPI\Client\Model\DisputeListResponse
```

List Disputes

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DisputeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$per_page = 56; // int | Number of records to fetch per page
$page = 56; // int | The section to retrieve
$status = 'status_example'; // string | Dispute Status. Acceptable values are awaiting-merchant-feedback, awaiting-bank-feedback, pending, resolved
$transaction = 'transaction_example'; // string | Transaction ID
$from = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | The start date
$to = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | The end date

try {
    $result = $apiInstance->disputeList($per_page, $page, $status, $transaction, $from, $to);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DisputeApi->disputeList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **per_page** | **int**| Number of records to fetch per page | [optional] |
| **page** | **int**| The section to retrieve | [optional] |
| **status** | **string**| Dispute Status. Acceptable values are awaiting-merchant-feedback, awaiting-bank-feedback, pending, resolved | [optional] |
| **transaction** | **string**| Transaction ID | [optional] |
| **from** | **\DateTime**| The start date | [optional] |
| **to** | **\DateTime**| The end date | [optional] |

### Return type

[**\OpenAPI\Client\Model\DisputeListResponse**](../Model/DisputeListResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `disputeResolve()`

```php
disputeResolve($id, $dispute_resolve): \OpenAPI\Client\Model\DisputeResolveResponse
```

Resolve a Dispute

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DisputeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Dispute ID
$dispute_resolve = new \OpenAPI\Client\Model\DisputeResolve(); // \OpenAPI\Client\Model\DisputeResolve

try {
    $result = $apiInstance->disputeResolve($id, $dispute_resolve);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DisputeApi->disputeResolve: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Dispute ID | |
| **dispute_resolve** | [**\OpenAPI\Client\Model\DisputeResolve**](../Model/DisputeResolve.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\DisputeResolveResponse**](../Model/DisputeResolveResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `disputeTransaction()`

```php
disputeTransaction($id): \OpenAPI\Client\Model\DisputeListTransactionResponse
```

List Transaction Disputes

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DisputeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Transaction ID

try {
    $result = $apiInstance->disputeTransaction($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DisputeApi->disputeTransaction: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Transaction ID | |

### Return type

[**\OpenAPI\Client\Model\DisputeListTransactionResponse**](../Model/DisputeListTransactionResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `disputeUpdate()`

```php
disputeUpdate($id, $dispute_update): \OpenAPI\Client\Model\DisputeUpdateResponse
```

Update Dispute

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DisputeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Dispute ID
$dispute_update = new \OpenAPI\Client\Model\DisputeUpdate(); // \OpenAPI\Client\Model\DisputeUpdate

try {
    $result = $apiInstance->disputeUpdate($id, $dispute_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DisputeApi->disputeUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Dispute ID | |
| **dispute_update** | [**\OpenAPI\Client\Model\DisputeUpdate**](../Model/DisputeUpdate.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\DisputeUpdateResponse**](../Model/DisputeUpdateResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `disputeUploadUrl()`

```php
disputeUploadUrl($id): \OpenAPI\Client\Model\DisputeUploadURLResponse
```

Get Upload URL

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DisputeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Dispute ID

try {
    $result = $apiInstance->disputeUploadUrl($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DisputeApi->disputeUploadUrl: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Dispute ID | |

### Return type

[**\OpenAPI\Client\Model\DisputeUploadURLResponse**](../Model/DisputeUploadURLResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
