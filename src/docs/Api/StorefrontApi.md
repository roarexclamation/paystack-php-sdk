# OpenAPI\Client\StorefrontApi

All URIs are relative to https://api.paystack.co, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**storefrontAddProducts()**](StorefrontApi.md#storefrontAddProducts) | **POST** /storefront/{id}/product | Add Products to Storefront |
| [**storefrontCreate()**](StorefrontApi.md#storefrontCreate) | **POST** /storefront | Create Storefront |
| [**storefrontDelete()**](StorefrontApi.md#storefrontDelete) | **DELETE** /storefront/{id} | Delete Storefront |
| [**storefrontDuplicate()**](StorefrontApi.md#storefrontDuplicate) | **POST** /storefront/{id}/duplicate | Duplicate Storefront |
| [**storefrontFetch()**](StorefrontApi.md#storefrontFetch) | **GET** /storefront/{id} | Fetch Storefront |
| [**storefrontFetchOrders()**](StorefrontApi.md#storefrontFetchOrders) | **GET** /storefront/{id}/order | Fetch Storefront Orders |
| [**storefrontList()**](StorefrontApi.md#storefrontList) | **GET** /storefront | List Storefronts |
| [**storefrontListProducts()**](StorefrontApi.md#storefrontListProducts) | **GET** /storefront/{id}/product | List Products in Storefront |
| [**storefrontPublish()**](StorefrontApi.md#storefrontPublish) | **POST** /storefront/{id}/publish | Publish Storefront |
| [**storefrontUpdate()**](StorefrontApi.md#storefrontUpdate) | **PUT** /storefront/{id} | Update Storefront |
| [**storefrontVerifySlug()**](StorefrontApi.md#storefrontVerifySlug) | **GET** /storefront/verify/{slug} | Verify Storefront Slug |


## `storefrontAddProducts()`

```php
storefrontAddProducts($id, $storefront_add_products): \OpenAPI\Client\Model\Response
```

Add Products to Storefront

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\StorefrontApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$storefront_add_products = new \OpenAPI\Client\Model\StorefrontAddProducts(); // \OpenAPI\Client\Model\StorefrontAddProducts

try {
    $result = $apiInstance->storefrontAddProducts($id, $storefront_add_products);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorefrontApi->storefrontAddProducts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |
| **storefront_add_products** | [**\OpenAPI\Client\Model\StorefrontAddProducts**](../Model/StorefrontAddProducts.md)|  | [optional] |

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

## `storefrontCreate()`

```php
storefrontCreate($storefront_create): \OpenAPI\Client\Model\StorefrontCreateResponse
```

Create Storefront

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\StorefrontApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$storefront_create = new \OpenAPI\Client\Model\StorefrontCreate(); // \OpenAPI\Client\Model\StorefrontCreate

try {
    $result = $apiInstance->storefrontCreate($storefront_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorefrontApi->storefrontCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **storefront_create** | [**\OpenAPI\Client\Model\StorefrontCreate**](../Model/StorefrontCreate.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\StorefrontCreateResponse**](../Model/StorefrontCreateResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storefrontDelete()`

```php
storefrontDelete($id): \OpenAPI\Client\Model\StorefrontDeleteResponse
```

Delete Storefront

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\StorefrontApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $result = $apiInstance->storefrontDelete($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorefrontApi->storefrontDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\StorefrontDeleteResponse**](../Model/StorefrontDeleteResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storefrontDuplicate()`

```php
storefrontDuplicate($id): \OpenAPI\Client\Model\Response
```

Duplicate Storefront

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\StorefrontApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $result = $apiInstance->storefrontDuplicate($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorefrontApi->storefrontDuplicate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

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

## `storefrontFetch()`

```php
storefrontFetch($id): \OpenAPI\Client\Model\StorefrontFetchResponse
```

Fetch Storefront

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\StorefrontApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $result = $apiInstance->storefrontFetch($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorefrontApi->storefrontFetch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\StorefrontFetchResponse**](../Model/StorefrontFetchResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storefrontFetchOrders()`

```php
storefrontFetchOrders($id): \OpenAPI\Client\Model\Response
```

Fetch Storefront Orders

Fetch all orders in your Storefront

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\StorefrontApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = Z0R4orOU; // string

try {
    $result = $apiInstance->storefrontFetchOrders($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorefrontApi->storefrontFetchOrders: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

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

## `storefrontList()`

```php
storefrontList($per_page, $page, $status): \OpenAPI\Client\Model\StorefrontListResponse
```

List Storefronts

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\StorefrontApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$per_page = 56; // int
$page = 56; // int
$status = 'status_example'; // string

try {
    $result = $apiInstance->storefrontList($per_page, $page, $status);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorefrontApi->storefrontList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **per_page** | **int**|  | [optional] |
| **page** | **int**|  | [optional] |
| **status** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\StorefrontListResponse**](../Model/StorefrontListResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storefrontListProducts()`

```php
storefrontListProducts($id): \OpenAPI\Client\Model\Response
```

List Products in Storefront

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\StorefrontApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $result = $apiInstance->storefrontListProducts($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorefrontApi->storefrontListProducts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

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

## `storefrontPublish()`

```php
storefrontPublish($id): \OpenAPI\Client\Model\Response
```

Publish Storefront

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\StorefrontApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $result = $apiInstance->storefrontPublish($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorefrontApi->storefrontPublish: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

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

## `storefrontUpdate()`

```php
storefrontUpdate($id, $storefront_update): \OpenAPI\Client\Model\StorefrontUpdateResponse
```

Update Storefront

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\StorefrontApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$storefront_update = new \OpenAPI\Client\Model\StorefrontUpdate(); // \OpenAPI\Client\Model\StorefrontUpdate

try {
    $result = $apiInstance->storefrontUpdate($id, $storefront_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorefrontApi->storefrontUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |
| **storefront_update** | [**\OpenAPI\Client\Model\StorefrontUpdate**](../Model/StorefrontUpdate.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\StorefrontUpdateResponse**](../Model/StorefrontUpdateResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storefrontVerifySlug()`

```php
storefrontVerifySlug($slug): \OpenAPI\Client\Model\Response
```

Verify Storefront Slug

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\StorefrontApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$slug = 'slug_example'; // string

try {
    $result = $apiInstance->storefrontVerifySlug($slug);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorefrontApi->storefrontVerifySlug: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **slug** | **string**|  | |

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
