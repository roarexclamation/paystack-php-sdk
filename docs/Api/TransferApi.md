# OpenAPI\Client\TransferApi

All URIs are relative to https://api.paystack.co, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**transferBulk()**](TransferApi.md#transferBulk) | **POST** /transfer/bulk | Initiate Bulk Transfer |
| [**transferDisableOtp()**](TransferApi.md#transferDisableOtp) | **POST** /transfer/disable_otp | Disable OTP requirement for Transfers |
| [**transferDisableOtpFinalize()**](TransferApi.md#transferDisableOtpFinalize) | **POST** /transfer/disable_otp_finalize | Finalize Disabling of OTP requirement for Transfers |
| [**transferDownload()**](TransferApi.md#transferDownload) | **GET** /transfer/export | Export Transfers |
| [**transferEnableOtp()**](TransferApi.md#transferEnableOtp) | **POST** /transfer/enable_otp | Enable OTP requirement for Transfers |
| [**transferFetch()**](TransferApi.md#transferFetch) | **GET** /transfer/{code} | Fetch Transfer |
| [**transferFinalize()**](TransferApi.md#transferFinalize) | **POST** /transfer/finalize_transfer | Finalize Transfer |
| [**transferInitiate()**](TransferApi.md#transferInitiate) | **POST** /transfer | Initiate Transfer |
| [**transferList()**](TransferApi.md#transferList) | **GET** /transfer | List Transfers |
| [**transferResendOtp()**](TransferApi.md#transferResendOtp) | **POST** /transfer/resend_otp | Resend OTP for Transfer |
| [**transferVerify()**](TransferApi.md#transferVerify) | **GET** /transfer/verify/{reference} | Verify Transfer |


## `transferBulk()`

```php
transferBulk($transfer_bulk): \OpenAPI\Client\Model\TransferBulkResponse
```

Initiate Bulk Transfer

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TransferApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$transfer_bulk = new \OpenAPI\Client\Model\TransferBulk(); // \OpenAPI\Client\Model\TransferBulk

try {
    $result = $apiInstance->transferBulk($transfer_bulk);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransferApi->transferBulk: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **transfer_bulk** | [**\OpenAPI\Client\Model\TransferBulk**](../Model/TransferBulk.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\TransferBulkResponse**](../Model/TransferBulkResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `transferDisableOtp()`

```php
transferDisableOtp(): \OpenAPI\Client\Model\TransferDisablesOtpResponse
```

Disable OTP requirement for Transfers

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TransferApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->transferDisableOtp();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransferApi->transferDisableOtp: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\TransferDisablesOtpResponse**](../Model/TransferDisablesOtpResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `transferDisableOtpFinalize()`

```php
transferDisableOtpFinalize($transfer_finalize_disable_otp): \OpenAPI\Client\Model\TransferFinalizeDisablesOtpResponse
```

Finalize Disabling of OTP requirement for Transfers

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TransferApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$transfer_finalize_disable_otp = new \OpenAPI\Client\Model\TransferFinalizeDisableOTP(); // \OpenAPI\Client\Model\TransferFinalizeDisableOTP

try {
    $result = $apiInstance->transferDisableOtpFinalize($transfer_finalize_disable_otp);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransferApi->transferDisableOtpFinalize: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **transfer_finalize_disable_otp** | [**\OpenAPI\Client\Model\TransferFinalizeDisableOTP**](../Model/TransferFinalizeDisableOTP.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\TransferFinalizeDisablesOtpResponse**](../Model/TransferFinalizeDisablesOtpResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `transferDownload()`

```php
transferDownload($per_page, $page, $status, $from, $to): \OpenAPI\Client\Model\Response
```

Export Transfers

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TransferApi(
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
    $result = $apiInstance->transferDownload($per_page, $page, $status, $from, $to);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransferApi->transferDownload: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\Response**](../Model/Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `transferEnableOtp()`

```php
transferEnableOtp(): \OpenAPI\Client\Model\TransferEnablesOtpResponse
```

Enable OTP requirement for Transfers

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TransferApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->transferEnableOtp();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransferApi->transferEnableOtp: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\TransferEnablesOtpResponse**](../Model/TransferEnablesOtpResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `transferFetch()`

```php
transferFetch($code): \OpenAPI\Client\Model\TransferFetchResponse
```

Fetch Transfer

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TransferApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$code = 'code_example'; // string | Transfer code

try {
    $result = $apiInstance->transferFetch($code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransferApi->transferFetch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**| Transfer code | |

### Return type

[**\OpenAPI\Client\Model\TransferFetchResponse**](../Model/TransferFetchResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `transferFinalize()`

```php
transferFinalize($transfer_finalize): \OpenAPI\Client\Model\Response
```

Finalize Transfer

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TransferApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$transfer_finalize = new \OpenAPI\Client\Model\TransferFinalize(); // \OpenAPI\Client\Model\TransferFinalize

try {
    $result = $apiInstance->transferFinalize($transfer_finalize);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransferApi->transferFinalize: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **transfer_finalize** | [**\OpenAPI\Client\Model\TransferFinalize**](../Model/TransferFinalize.md)|  | [optional] |

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

## `transferInitiate()`

```php
transferInitiate($transfer_initiate): \OpenAPI\Client\Model\TransferCreateResponse
```

Initiate Transfer

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TransferApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$transfer_initiate = new \OpenAPI\Client\Model\TransferInitiate(); // \OpenAPI\Client\Model\TransferInitiate

try {
    $result = $apiInstance->transferInitiate($transfer_initiate);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransferApi->transferInitiate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **transfer_initiate** | [**\OpenAPI\Client\Model\TransferInitiate**](../Model/TransferInitiate.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\TransferCreateResponse**](../Model/TransferCreateResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `transferList()`

```php
transferList($per_page, $page, $status, $from, $to): \OpenAPI\Client\Model\TransferListResponse
```

List Transfers

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TransferApi(
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
    $result = $apiInstance->transferList($per_page, $page, $status, $from, $to);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransferApi->transferList: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\TransferListResponse**](../Model/TransferListResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `transferResendOtp()`

```php
transferResendOtp($transfer_resend_otp): \OpenAPI\Client\Model\TransferResendsOtpResponse
```

Resend OTP for Transfer

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TransferApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$transfer_resend_otp = new \OpenAPI\Client\Model\TransferResendOTP(); // \OpenAPI\Client\Model\TransferResendOTP

try {
    $result = $apiInstance->transferResendOtp($transfer_resend_otp);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransferApi->transferResendOtp: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **transfer_resend_otp** | [**\OpenAPI\Client\Model\TransferResendOTP**](../Model/TransferResendOTP.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\TransferResendsOtpResponse**](../Model/TransferResendsOtpResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `transferVerify()`

```php
transferVerify($reference): \OpenAPI\Client\Model\TransferVerifyResponse
```

Verify Transfer

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TransferApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$reference = 'reference_example'; // string

try {
    $result = $apiInstance->transferVerify($reference);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransferApi->transferVerify: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **reference** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\TransferVerifyResponse**](../Model/TransferVerifyResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
