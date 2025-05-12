# OpenAPI\Client\CustomerApi

All URIs are relative to https://api.paystack.co, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**customerCreate()**](CustomerApi.md#customerCreate) | **POST** /customer | Create Customer |
| [**customerDeactivateAuthorization()**](CustomerApi.md#customerDeactivateAuthorization) | **POST** /customer/deactivate_authorization | Deactivate Authorization |
| [**customerFetch()**](CustomerApi.md#customerFetch) | **GET** /customer/{code} | Fetch Customer |
| [**customerList()**](CustomerApi.md#customerList) | **GET** /customer | List Customers |
| [**customerRiskAction()**](CustomerApi.md#customerRiskAction) | **POST** /customer/set_risk_action | White/blacklist Customer |
| [**customerUpdate()**](CustomerApi.md#customerUpdate) | **PUT** /customer/{code} | Update Customer |
| [**customerValidate()**](CustomerApi.md#customerValidate) | **POST** /customer/{code}/identification | Validate Customer |


## `customerCreate()`

```php
customerCreate($customer_create): \OpenAPI\Client\Model\CustomerCreateResponse
```

Create Customer

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$customer_create = new \OpenAPI\Client\Model\CustomerCreate(); // \OpenAPI\Client\Model\CustomerCreate

try {
    $result = $apiInstance->customerCreate($customer_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerApi->customerCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **customer_create** | [**\OpenAPI\Client\Model\CustomerCreate**](../Model/CustomerCreate.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\CustomerCreateResponse**](../Model/CustomerCreateResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `customerDeactivateAuthorization()`

```php
customerDeactivateAuthorization($customer_deactivate_authorization): \OpenAPI\Client\Model\CustomerDeactivateAuthorizationResponse
```

Deactivate Authorization

Deactivate a customer's card

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$customer_deactivate_authorization = new \OpenAPI\Client\Model\CustomerDeactivateAuthorization(); // \OpenAPI\Client\Model\CustomerDeactivateAuthorization

try {
    $result = $apiInstance->customerDeactivateAuthorization($customer_deactivate_authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerApi->customerDeactivateAuthorization: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **customer_deactivate_authorization** | [**\OpenAPI\Client\Model\CustomerDeactivateAuthorization**](../Model/CustomerDeactivateAuthorization.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\CustomerDeactivateAuthorizationResponse**](../Model/CustomerDeactivateAuthorizationResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `customerFetch()`

```php
customerFetch($code): \OpenAPI\Client\Model\CustomerFetchResponse
```

Fetch Customer

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$code = 'code_example'; // string

try {
    $result = $apiInstance->customerFetch($code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerApi->customerFetch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\CustomerFetchResponse**](../Model/CustomerFetchResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `customerList()`

```php
customerList($use_cursor, $next, $previous, $from, $to, $per_page, $page): \OpenAPI\Client\Model\CustomerListResponse
```

List Customers

List customers on your integration

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$use_cursor = True; // bool
$next = 'next_example'; // string
$previous = 'previous_example'; // string
$from = 'from_example'; // string
$to = 'to_example'; // string
$per_page = 'per_page_example'; // string
$page = 'page_example'; // string

try {
    $result = $apiInstance->customerList($use_cursor, $next, $previous, $from, $to, $per_page, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerApi->customerList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **use_cursor** | **bool**|  | [optional] |
| **next** | **string**|  | [optional] |
| **previous** | **string**|  | [optional] |
| **from** | **string**|  | [optional] |
| **to** | **string**|  | [optional] |
| **per_page** | **string**|  | [optional] |
| **page** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\CustomerListResponse**](../Model/CustomerListResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `customerRiskAction()`

```php
customerRiskAction($customer_risk_action): \OpenAPI\Client\Model\CustomerWhitelistBlacklistResponse
```

White/blacklist Customer

Set customer's risk action by whitelisting or blacklisting the customer

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$customer_risk_action = new \OpenAPI\Client\Model\CustomerRiskAction(); // \OpenAPI\Client\Model\CustomerRiskAction

try {
    $result = $apiInstance->customerRiskAction($customer_risk_action);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerApi->customerRiskAction: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **customer_risk_action** | [**\OpenAPI\Client\Model\CustomerRiskAction**](../Model/CustomerRiskAction.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\CustomerWhitelistBlacklistResponse**](../Model/CustomerWhitelistBlacklistResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `customerUpdate()`

```php
customerUpdate($code, $customer_update): \OpenAPI\Client\Model\CustomerUpdateResponse
```

Update Customer

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$code = 'code_example'; // string
$customer_update = new \OpenAPI\Client\Model\CustomerUpdate(); // \OpenAPI\Client\Model\CustomerUpdate

try {
    $result = $apiInstance->customerUpdate($code, $customer_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerApi->customerUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**|  | |
| **customer_update** | [**\OpenAPI\Client\Model\CustomerUpdate**](../Model/CustomerUpdate.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\CustomerUpdateResponse**](../Model/CustomerUpdateResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `customerValidate()`

```php
customerValidate($code, $customer_validate): \OpenAPI\Client\Model\CustomerValidateResponse
```

Validate Customer

Validate a customer's identity

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$code = 'code_example'; // string
$customer_validate = new \OpenAPI\Client\Model\CustomerValidate(); // \OpenAPI\Client\Model\CustomerValidate

try {
    $result = $apiInstance->customerValidate($code, $customer_validate);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerApi->customerValidate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**|  | |
| **customer_validate** | [**\OpenAPI\Client\Model\CustomerValidate**](../Model/CustomerValidate.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\CustomerValidateResponse**](../Model/CustomerValidateResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
