# OpenAPI\Client\PaymentRequestApi

All URIs are relative to https://api.paystack.co, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**paymentRequestArchive()**](PaymentRequestApi.md#paymentRequestArchive) | **POST** /paymentrequest/archive/{id} | Archive Payment Request |
| [**paymentRequestCreate()**](PaymentRequestApi.md#paymentRequestCreate) | **POST** /paymentrequest | Create Payment Request |
| [**paymentRequestFetch()**](PaymentRequestApi.md#paymentRequestFetch) | **GET** /paymentrequest/{id} | Fetch Payment Request |
| [**paymentRequestFinalize()**](PaymentRequestApi.md#paymentRequestFinalize) | **POST** /paymentrequest/finalize/{id} | Finalize Payment Request |
| [**paymentRequestList()**](PaymentRequestApi.md#paymentRequestList) | **GET** /paymentrequest | List Payment Request |
| [**paymentRequestNotify()**](PaymentRequestApi.md#paymentRequestNotify) | **POST** /paymentrequest/notify/{id} | Send Notification |
| [**paymentRequestTotals()**](PaymentRequestApi.md#paymentRequestTotals) | **GET** /paymentrequest/totals | Payment Request Total |
| [**paymentRequestUpdate()**](PaymentRequestApi.md#paymentRequestUpdate) | **PUT** /paymentrequest/{id} | Update Payment Request |
| [**paymentRequestVerify()**](PaymentRequestApi.md#paymentRequestVerify) | **GET** /paymentrequest/verify/{id} | Verify Payment Request |


## `paymentRequestArchive()`

```php
paymentRequestArchive($id): \OpenAPI\Client\Model\PaymentRequestArchiveResponse
```

Archive Payment Request

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PaymentRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $result = $apiInstance->paymentRequestArchive($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentRequestApi->paymentRequestArchive: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\PaymentRequestArchiveResponse**](../Model/PaymentRequestArchiveResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `paymentRequestCreate()`

```php
paymentRequestCreate($payment_request_create): \OpenAPI\Client\Model\PaymentRequestCreateResponse
```

Create Payment Request

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PaymentRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_request_create = new \OpenAPI\Client\Model\PaymentRequestCreate(); // \OpenAPI\Client\Model\PaymentRequestCreate

try {
    $result = $apiInstance->paymentRequestCreate($payment_request_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentRequestApi->paymentRequestCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_request_create** | [**\OpenAPI\Client\Model\PaymentRequestCreate**](../Model/PaymentRequestCreate.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PaymentRequestCreateResponse**](../Model/PaymentRequestCreateResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `paymentRequestFetch()`

```php
paymentRequestFetch($id): \OpenAPI\Client\Model\PaymentRequestListResponse
```

Fetch Payment Request

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PaymentRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $result = $apiInstance->paymentRequestFetch($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentRequestApi->paymentRequestFetch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\PaymentRequestListResponse**](../Model/PaymentRequestListResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `paymentRequestFinalize()`

```php
paymentRequestFinalize($id): \OpenAPI\Client\Model\PaymentRequestFinalizeResponse
```

Finalize Payment Request

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PaymentRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $result = $apiInstance->paymentRequestFinalize($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentRequestApi->paymentRequestFinalize: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\PaymentRequestFinalizeResponse**](../Model/PaymentRequestFinalizeResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `paymentRequestList()`

```php
paymentRequestList($per_page, $page, $customer, $status, $currency, $from, $to): \OpenAPI\Client\Model\PaymentRequestListResponse
```

List Payment Request

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PaymentRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$per_page = 56; // int | Number of records to fetch per page
$page = 56; // int | The section to retrieve
$customer = 'customer_example'; // string | Customer ID
$status = 'status_example'; // string | Invoice status to filter
$currency = 'currency_example'; // string | If your integration supports more than one currency, choose the one to filter
$from = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | The start date
$to = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | The end date

try {
    $result = $apiInstance->paymentRequestList($per_page, $page, $customer, $status, $currency, $from, $to);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentRequestApi->paymentRequestList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **per_page** | **int**| Number of records to fetch per page | [optional] |
| **page** | **int**| The section to retrieve | [optional] |
| **customer** | **string**| Customer ID | [optional] |
| **status** | **string**| Invoice status to filter | [optional] |
| **currency** | **string**| If your integration supports more than one currency, choose the one to filter | [optional] |
| **from** | **\DateTime**| The start date | [optional] |
| **to** | **\DateTime**| The end date | [optional] |

### Return type

[**\OpenAPI\Client\Model\PaymentRequestListResponse**](../Model/PaymentRequestListResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `paymentRequestNotify()`

```php
paymentRequestNotify($id): \OpenAPI\Client\Model\PaymentRequestSendNotificationResponse
```

Send Notification

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PaymentRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $result = $apiInstance->paymentRequestNotify($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentRequestApi->paymentRequestNotify: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\PaymentRequestSendNotificationResponse**](../Model/PaymentRequestSendNotificationResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `paymentRequestTotals()`

```php
paymentRequestTotals(): \OpenAPI\Client\Model\PaymentRequestTotalResponse
```

Payment Request Total

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PaymentRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->paymentRequestTotals();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentRequestApi->paymentRequestTotals: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\PaymentRequestTotalResponse**](../Model/PaymentRequestTotalResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `paymentRequestUpdate()`

```php
paymentRequestUpdate($id, $payment_request_update): \OpenAPI\Client\Model\PaymentRequestUpdateResponse
```

Update Payment Request

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PaymentRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$payment_request_update = new \OpenAPI\Client\Model\PaymentRequestUpdate(); // \OpenAPI\Client\Model\PaymentRequestUpdate

try {
    $result = $apiInstance->paymentRequestUpdate($id, $payment_request_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentRequestApi->paymentRequestUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |
| **payment_request_update** | [**\OpenAPI\Client\Model\PaymentRequestUpdate**](../Model/PaymentRequestUpdate.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PaymentRequestUpdateResponse**](../Model/PaymentRequestUpdateResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `paymentRequestVerify()`

```php
paymentRequestVerify($id): \OpenAPI\Client\Model\PaymentRequestVerifyResponse
```

Verify Payment Request

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PaymentRequestApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $result = $apiInstance->paymentRequestVerify($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentRequestApi->paymentRequestVerify: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\PaymentRequestVerifyResponse**](../Model/PaymentRequestVerifyResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
