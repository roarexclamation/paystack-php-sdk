# OpenAPI\Client\IntegrationApi

All URIs are relative to https://api.paystack.co, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**integrationFetchPaymentSessionTimeout()**](IntegrationApi.md#integrationFetchPaymentSessionTimeout) | **GET** /integration/payment_session_timeout | Fetch Payment Session Timeout |
| [**integrationUpdatePaymentSessionTimeout()**](IntegrationApi.md#integrationUpdatePaymentSessionTimeout) | **PUT** /integration/payment_session_timeout | Update Payment Session Timeout |


## `integrationFetchPaymentSessionTimeout()`

```php
integrationFetchPaymentSessionTimeout(): \OpenAPI\Client\Model\Response
```

Fetch Payment Session Timeout

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\IntegrationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->integrationFetchPaymentSessionTimeout();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationApi->integrationFetchPaymentSessionTimeout: ', $e->getMessage(), PHP_EOL;
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

## `integrationUpdatePaymentSessionTimeout()`

```php
integrationUpdatePaymentSessionTimeout($payment_session): \OpenAPI\Client\Model\Response
```

Update Payment Session Timeout

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\IntegrationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_session = new \OpenAPI\Client\Model\PaymentSession(); // \OpenAPI\Client\Model\PaymentSession

try {
    $result = $apiInstance->integrationUpdatePaymentSessionTimeout($payment_session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationApi->integrationUpdatePaymentSessionTimeout: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_session** | [**\OpenAPI\Client\Model\PaymentSession**](../Model/PaymentSession.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\Response**](../Model/Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
