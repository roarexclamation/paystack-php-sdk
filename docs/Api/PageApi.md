# OpenAPI\Client\PageApi

All URIs are relative to https://api.paystack.co, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**pageAddProducts()**](PageApi.md#pageAddProducts) | **POST** /page/{id}/product | Add Products |
| [**pageCheckSlugAvailability()**](PageApi.md#pageCheckSlugAvailability) | **GET** /page/check_slug_availability/{slug} | Check Slug Availability |
| [**pageCreate()**](PageApi.md#pageCreate) | **POST** /page | Create Page |
| [**pageFetch()**](PageApi.md#pageFetch) | **GET** /page/{id} | Fetch Page |
| [**pageList()**](PageApi.md#pageList) | **GET** /page | List Pages |
| [**pageUpdate()**](PageApi.md#pageUpdate) | **PUT** /page/{id} | Update Page |


## `pageAddProducts()`

```php
pageAddProducts($id, $page_product): \OpenAPI\Client\Model\PageAddProductsResponse
```

Add Products

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$page_product = new \OpenAPI\Client\Model\PageProduct(); // \OpenAPI\Client\Model\PageProduct

try {
    $result = $apiInstance->pageAddProducts($id, $page_product);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PageApi->pageAddProducts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |
| **page_product** | [**\OpenAPI\Client\Model\PageProduct**](../Model/PageProduct.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PageAddProductsResponse**](../Model/PageAddProductsResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pageCheckSlugAvailability()`

```php
pageCheckSlugAvailability($slug): \OpenAPI\Client\Model\PageCheckSlugAvailabilityResponse
```

Check Slug Availability

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$slug = 'slug_example'; // string

try {
    $result = $apiInstance->pageCheckSlugAvailability($slug);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PageApi->pageCheckSlugAvailability: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **slug** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\PageCheckSlugAvailabilityResponse**](../Model/PageCheckSlugAvailabilityResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pageCreate()`

```php
pageCreate($page_create): \OpenAPI\Client\Model\PageCreateResponse
```

Create Page

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page_create = new \OpenAPI\Client\Model\PageCreate(); // \OpenAPI\Client\Model\PageCreate

try {
    $result = $apiInstance->pageCreate($page_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PageApi->pageCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page_create** | [**\OpenAPI\Client\Model\PageCreate**](../Model/PageCreate.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PageCreateResponse**](../Model/PageCreateResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pageFetch()`

```php
pageFetch($id): \OpenAPI\Client\Model\PageFetchResponse
```

Fetch Page

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $result = $apiInstance->pageFetch($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PageApi->pageFetch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\PageFetchResponse**](../Model/PageFetchResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pageList()`

```php
pageList($per_page, $page, $from, $to): \OpenAPI\Client\Model\PageListResponse
```

List Pages

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PageApi(
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
    $result = $apiInstance->pageList($per_page, $page, $from, $to);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PageApi->pageList: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\PageListResponse**](../Model/PageListResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pageUpdate()`

```php
pageUpdate($id, $page_update): \OpenAPI\Client\Model\PageUpdateResponse
```

Update Page

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$page_update = new \OpenAPI\Client\Model\PageUpdate(); // \OpenAPI\Client\Model\PageUpdate

try {
    $result = $apiInstance->pageUpdate($id, $page_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PageApi->pageUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |
| **page_update** | [**\OpenAPI\Client\Model\PageUpdate**](../Model/PageUpdate.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PageUpdateResponse**](../Model/PageUpdateResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
