# OpenAPI\Client\ChargeApi

All URIs are relative to https://api.paystack.co, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**chargeCheck()**](ChargeApi.md#chargeCheck) | **GET** /charge/{reference} | Check pending charge |
| [**chargeCreate()**](ChargeApi.md#chargeCreate) | **POST** /charge | Create Charge |
| [**chargeSubmitAddress()**](ChargeApi.md#chargeSubmitAddress) | **POST** /charge/submit_address | Submit Address |
| [**chargeSubmitBirthday()**](ChargeApi.md#chargeSubmitBirthday) | **POST** /charge/submit_birthday | Submit Birthday |
| [**chargeSubmitOtp()**](ChargeApi.md#chargeSubmitOtp) | **POST** /charge/submit_otp | Submit OTP |
| [**chargeSubmitPhone()**](ChargeApi.md#chargeSubmitPhone) | **POST** /charge/submit_phone | Submit Phone |
| [**chargeSubmitPin()**](ChargeApi.md#chargeSubmitPin) | **POST** /charge/submit_pin | Submit PIN |


## `chargeCheck()`

```php
chargeCheck($reference): \OpenAPI\Client\Model\ChargeCheckPendingResponse
```

Check pending charge

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ChargeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$reference = 'reference_example'; // string

try {
    $result = $apiInstance->chargeCheck($reference);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChargeApi->chargeCheck: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **reference** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\ChargeCheckPendingResponse**](../Model/ChargeCheckPendingResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `chargeCreate()`

```php
chargeCreate($charge_create_request): \OpenAPI\Client\Model\ChargeCreateResponse
```

Create Charge

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ChargeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$charge_create_request = new \OpenAPI\Client\Model\ChargeCreateRequest(); // \OpenAPI\Client\Model\ChargeCreateRequest

try {
    $result = $apiInstance->chargeCreate($charge_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChargeApi->chargeCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **charge_create_request** | [**\OpenAPI\Client\Model\ChargeCreateRequest**](../Model/ChargeCreateRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ChargeCreateResponse**](../Model/ChargeCreateResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `chargeSubmitAddress()`

```php
chargeSubmitAddress($charge_submit_address): \OpenAPI\Client\Model\Response
```

Submit Address

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ChargeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$charge_submit_address = new \OpenAPI\Client\Model\ChargeSubmitAddress(); // \OpenAPI\Client\Model\ChargeSubmitAddress

try {
    $result = $apiInstance->chargeSubmitAddress($charge_submit_address);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChargeApi->chargeSubmitAddress: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **charge_submit_address** | [**\OpenAPI\Client\Model\ChargeSubmitAddress**](../Model/ChargeSubmitAddress.md)|  | [optional] |

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

## `chargeSubmitBirthday()`

```php
chargeSubmitBirthday($charge_submit_birthday): \OpenAPI\Client\Model\ChargeSubmitBirthdayResponse
```

Submit Birthday

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ChargeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$charge_submit_birthday = new \OpenAPI\Client\Model\ChargeSubmitBirthday(); // \OpenAPI\Client\Model\ChargeSubmitBirthday

try {
    $result = $apiInstance->chargeSubmitBirthday($charge_submit_birthday);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChargeApi->chargeSubmitBirthday: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **charge_submit_birthday** | [**\OpenAPI\Client\Model\ChargeSubmitBirthday**](../Model/ChargeSubmitBirthday.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ChargeSubmitBirthdayResponse**](../Model/ChargeSubmitBirthdayResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `chargeSubmitOtp()`

```php
chargeSubmitOtp($charge_submit_otp): \OpenAPI\Client\Model\ChargeSubmitOtpResponse
```

Submit OTP

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ChargeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$charge_submit_otp = new \OpenAPI\Client\Model\ChargeSubmitOTP(); // \OpenAPI\Client\Model\ChargeSubmitOTP

try {
    $result = $apiInstance->chargeSubmitOtp($charge_submit_otp);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChargeApi->chargeSubmitOtp: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **charge_submit_otp** | [**\OpenAPI\Client\Model\ChargeSubmitOTP**](../Model/ChargeSubmitOTP.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ChargeSubmitOtpResponse**](../Model/ChargeSubmitOtpResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `chargeSubmitPhone()`

```php
chargeSubmitPhone($charge_submit_phone): \OpenAPI\Client\Model\ChargeSubmitPhoneResponse
```

Submit Phone

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ChargeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$charge_submit_phone = new \OpenAPI\Client\Model\ChargeSubmitPhone(); // \OpenAPI\Client\Model\ChargeSubmitPhone

try {
    $result = $apiInstance->chargeSubmitPhone($charge_submit_phone);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChargeApi->chargeSubmitPhone: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **charge_submit_phone** | [**\OpenAPI\Client\Model\ChargeSubmitPhone**](../Model/ChargeSubmitPhone.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ChargeSubmitPhoneResponse**](../Model/ChargeSubmitPhoneResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `chargeSubmitPin()`

```php
chargeSubmitPin($charge_submit_pin): \OpenAPI\Client\Model\ChargeSubmitPinResponse
```

Submit PIN

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ChargeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$charge_submit_pin = new \OpenAPI\Client\Model\ChargeSubmitPin(); // \OpenAPI\Client\Model\ChargeSubmitPin

try {
    $result = $apiInstance->chargeSubmitPin($charge_submit_pin);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChargeApi->chargeSubmitPin: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **charge_submit_pin** | [**\OpenAPI\Client\Model\ChargeSubmitPin**](../Model/ChargeSubmitPin.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ChargeSubmitPinResponse**](../Model/ChargeSubmitPinResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
