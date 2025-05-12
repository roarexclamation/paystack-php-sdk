# OpenAPI\Client\SubscriptionApi

All URIs are relative to https://api.paystack.co, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**subscriptionCreate()**](SubscriptionApi.md#subscriptionCreate) | **POST** /subscription | Create Subscription |
| [**subscriptionDisable()**](SubscriptionApi.md#subscriptionDisable) | **POST** /subscription/disable | Disable Subscription |
| [**subscriptionEnable()**](SubscriptionApi.md#subscriptionEnable) | **POST** /subscription/enable | Enable Subscription |
| [**subscriptionFetch()**](SubscriptionApi.md#subscriptionFetch) | **GET** /subscription/{code} | Fetch Subscription |
| [**subscriptionList()**](SubscriptionApi.md#subscriptionList) | **GET** /subscription | List Subscriptions |
| [**subscriptionManageEmail()**](SubscriptionApi.md#subscriptionManageEmail) | **POST** /subscription/{code}/manage/email | Send Update Subscription Link |
| [**subscriptionManageLink()**](SubscriptionApi.md#subscriptionManageLink) | **GET** /subscription/{code}/manage/link | Generate Update Subscription Link |


## `subscriptionCreate()`

```php
subscriptionCreate($subscription_create): \OpenAPI\Client\Model\SubscriptionCreateResponse
```

Create Subscription

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SubscriptionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$subscription_create = new \OpenAPI\Client\Model\SubscriptionCreate(); // \OpenAPI\Client\Model\SubscriptionCreate

try {
    $result = $apiInstance->subscriptionCreate($subscription_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubscriptionApi->subscriptionCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **subscription_create** | [**\OpenAPI\Client\Model\SubscriptionCreate**](../Model/SubscriptionCreate.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\SubscriptionCreateResponse**](../Model/SubscriptionCreateResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `subscriptionDisable()`

```php
subscriptionDisable($subscription_toggle): \OpenAPI\Client\Model\SubscriptionDisableResponse
```

Disable Subscription

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SubscriptionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$subscription_toggle = new \OpenAPI\Client\Model\SubscriptionToggle(); // \OpenAPI\Client\Model\SubscriptionToggle

try {
    $result = $apiInstance->subscriptionDisable($subscription_toggle);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubscriptionApi->subscriptionDisable: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **subscription_toggle** | [**\OpenAPI\Client\Model\SubscriptionToggle**](../Model/SubscriptionToggle.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\SubscriptionDisableResponse**](../Model/SubscriptionDisableResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `subscriptionEnable()`

```php
subscriptionEnable($subscription_toggle): \OpenAPI\Client\Model\Response
```

Enable Subscription

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SubscriptionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$subscription_toggle = new \OpenAPI\Client\Model\SubscriptionToggle(); // \OpenAPI\Client\Model\SubscriptionToggle

try {
    $result = $apiInstance->subscriptionEnable($subscription_toggle);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubscriptionApi->subscriptionEnable: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **subscription_toggle** | [**\OpenAPI\Client\Model\SubscriptionToggle**](../Model/SubscriptionToggle.md)|  | [optional] |

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

## `subscriptionFetch()`

```php
subscriptionFetch($code): \OpenAPI\Client\Model\SubscriptionFetchResponse
```

Fetch Subscription

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SubscriptionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$code = 'code_example'; // string

try {
    $result = $apiInstance->subscriptionFetch($code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubscriptionApi->subscriptionFetch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\SubscriptionFetchResponse**](../Model/SubscriptionFetchResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `subscriptionList()`

```php
subscriptionList($per_page, $page, $plan, $customer, $from, $to): \OpenAPI\Client\Model\SubscriptionListResponse
```

List Subscriptions

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SubscriptionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$per_page = 56; // int | Number of records to fetch per page
$page = 56; // int | The section to retrieve
$plan = 'plan_example'; // string | Plan ID
$customer = 'customer_example'; // string | Customer ID
$from = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | The start date
$to = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | The end date

try {
    $result = $apiInstance->subscriptionList($per_page, $page, $plan, $customer, $from, $to);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubscriptionApi->subscriptionList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **per_page** | **int**| Number of records to fetch per page | [optional] |
| **page** | **int**| The section to retrieve | [optional] |
| **plan** | **string**| Plan ID | [optional] |
| **customer** | **string**| Customer ID | [optional] |
| **from** | **\DateTime**| The start date | [optional] |
| **to** | **\DateTime**| The end date | [optional] |

### Return type

[**\OpenAPI\Client\Model\SubscriptionListResponse**](../Model/SubscriptionListResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `subscriptionManageEmail()`

```php
subscriptionManageEmail($code): \OpenAPI\Client\Model\Response
```

Send Update Subscription Link

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SubscriptionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$code = 'code_example'; // string

try {
    $result = $apiInstance->subscriptionManageEmail($code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubscriptionApi->subscriptionManageEmail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**|  | |

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

## `subscriptionManageLink()`

```php
subscriptionManageLink($code): \OpenAPI\Client\Model\Response
```

Generate Update Subscription Link

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SubscriptionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$code = 'code_example'; // string

try {
    $result = $apiInstance->subscriptionManageLink($code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubscriptionApi->subscriptionManageLink: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**|  | |

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
