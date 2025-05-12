# OpenAPI\Client\BankApi

All URIs are relative to https://api.paystack.co, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**bankList()**](BankApi.md#bankList) | **GET** /bank | List Banks |
| [**bankResolveAccountNumber()**](BankApi.md#bankResolveAccountNumber) | **GET** /bank/resolve | Resolve Account Number |
| [**bankValidateAccountNumber()**](BankApi.md#bankValidateAccountNumber) | **POST** /bank/validate | Validate Bank Account |


## `bankList()`

```php
bankList($country, $pay_with_bank_transfer, $use_cursor, $per_page, $next, $previous, $gateway): \OpenAPI\Client\Model\MiscellaneousListBanksResponse
```

List Banks

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BankApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$country = 'country_example'; // string
$pay_with_bank_transfer = True; // bool
$use_cursor = True; // bool
$per_page = 56; // int
$next = 'next_example'; // string
$previous = 'previous_example'; // string
$gateway = 'gateway_example'; // string

try {
    $result = $apiInstance->bankList($country, $pay_with_bank_transfer, $use_cursor, $per_page, $next, $previous, $gateway);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BankApi->bankList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **country** | **string**|  | [optional] |
| **pay_with_bank_transfer** | **bool**|  | [optional] |
| **use_cursor** | **bool**|  | [optional] |
| **per_page** | **int**|  | [optional] |
| **next** | **string**|  | [optional] |
| **previous** | **string**|  | [optional] |
| **gateway** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\MiscellaneousListBanksResponse**](../Model/MiscellaneousListBanksResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `bankResolveAccountNumber()`

```php
bankResolveAccountNumber($account_number, $bank_code): \OpenAPI\Client\Model\VerificationResolveAccountNumberResponse
```

Resolve Account Number

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BankApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_number = 22728151; // int
$bank_code = 63; // int

try {
    $result = $apiInstance->bankResolveAccountNumber($account_number, $bank_code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BankApi->bankResolveAccountNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_number** | **int**|  | [optional] |
| **bank_code** | **int**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\VerificationResolveAccountNumberResponse**](../Model/VerificationResolveAccountNumberResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `bankValidateAccountNumber()`

```php
bankValidateAccountNumber($bank_validate_request): \OpenAPI\Client\Model\VerificationValidateAccountResponse
```

Validate Bank Account

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BankApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$bank_validate_request = new \OpenAPI\Client\Model\BankValidateRequest(); // \OpenAPI\Client\Model\BankValidateRequest

try {
    $result = $apiInstance->bankValidateAccountNumber($bank_validate_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BankApi->bankValidateAccountNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **bank_validate_request** | [**\OpenAPI\Client\Model\BankValidateRequest**](../Model/BankValidateRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\VerificationValidateAccountResponse**](../Model/VerificationValidateAccountResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
