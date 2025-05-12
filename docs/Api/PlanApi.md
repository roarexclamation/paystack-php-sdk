# OpenAPI\Client\PlanApi

All URIs are relative to https://api.paystack.co, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**planCreate()**](PlanApi.md#planCreate) | **POST** /plan | Create Plan |
| [**planFetch()**](PlanApi.md#planFetch) | **GET** /plan/{code} | Fetch Plan |
| [**planList()**](PlanApi.md#planList) | **GET** /plan | List Plans |
| [**planUpdate()**](PlanApi.md#planUpdate) | **PUT** /plan/{code} | Update Plan |


## `planCreate()`

```php
planCreate($plan_create): \OpenAPI\Client\Model\PlanCreateResponse
```

Create Plan

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PlanApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$plan_create = new \OpenAPI\Client\Model\PlanCreate(); // \OpenAPI\Client\Model\PlanCreate

try {
    $result = $apiInstance->planCreate($plan_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PlanApi->planCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **plan_create** | [**\OpenAPI\Client\Model\PlanCreate**](../Model/PlanCreate.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PlanCreateResponse**](../Model/PlanCreateResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `planFetch()`

```php
planFetch($code): \OpenAPI\Client\Model\PlanFetchResponse
```

Fetch Plan

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PlanApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$code = 'code_example'; // string

try {
    $result = $apiInstance->planFetch($code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PlanApi->planFetch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\PlanFetchResponse**](../Model/PlanFetchResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `planList()`

```php
planList($per_page, $page, $interval, $amount, $from, $to): \OpenAPI\Client\Model\PlanListResponse
```

List Plans

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PlanApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$per_page = 56; // int | Number of records to fetch per page
$page = 56; // int | The section to retrieve
$interval = 'interval_example'; // string | Specify interval of the plan
$amount = 56; // int | The amount on the plans to retrieve
$from = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | The start date
$to = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | The end date

try {
    $result = $apiInstance->planList($per_page, $page, $interval, $amount, $from, $to);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PlanApi->planList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **per_page** | **int**| Number of records to fetch per page | [optional] |
| **page** | **int**| The section to retrieve | [optional] |
| **interval** | **string**| Specify interval of the plan | [optional] |
| **amount** | **int**| The amount on the plans to retrieve | [optional] |
| **from** | **\DateTime**| The start date | [optional] |
| **to** | **\DateTime**| The end date | [optional] |

### Return type

[**\OpenAPI\Client\Model\PlanListResponse**](../Model/PlanListResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `planUpdate()`

```php
planUpdate($code, $plan_update): \OpenAPI\Client\Model\PlanUpdateResponse
```

Update Plan

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PlanApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$code = 'code_example'; // string
$plan_update = new \OpenAPI\Client\Model\PlanUpdate(); // \OpenAPI\Client\Model\PlanUpdate

try {
    $result = $apiInstance->planUpdate($code, $plan_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PlanApi->planUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**|  | |
| **plan_update** | [**\OpenAPI\Client\Model\PlanUpdate**](../Model/PlanUpdate.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PlanUpdateResponse**](../Model/PlanUpdateResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
