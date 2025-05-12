# OpenAPI\Client\TerminalApi

All URIs are relative to https://api.paystack.co, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**terminalCommission()**](TerminalApi.md#terminalCommission) | **POST** /terminal/commission_device | Commission Terminal |
| [**terminalDecommission()**](TerminalApi.md#terminalDecommission) | **POST** /terminal/decommission_device | Decommission Terminal |
| [**terminalFetch()**](TerminalApi.md#terminalFetch) | **GET** /terminal/{terminal_id} | Fetch Terminal |
| [**terminalFetchEventStatus()**](TerminalApi.md#terminalFetchEventStatus) | **GET** /terminal/{terminal_id}/event/{event_id} | Fetch Event Status |
| [**terminalFetchTerminalStatus()**](TerminalApi.md#terminalFetchTerminalStatus) | **GET** /terminal/{terminal_id}/presence | Fetch Terminal Status |
| [**terminalList()**](TerminalApi.md#terminalList) | **GET** /terminal | List Terminals |
| [**terminalSendEvent()**](TerminalApi.md#terminalSendEvent) | **POST** /terminal/{id}/event | Send Event |
| [**terminalUpdate()**](TerminalApi.md#terminalUpdate) | **PUT** /terminal/{terminal_id} | Update Terminal |


## `terminalCommission()`

```php
terminalCommission($terminal_activation_toggle): \OpenAPI\Client\Model\TerminalCommissionDeviceResponse
```

Commission Terminal

Activate your debug device by linking it to your integration

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TerminalApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$terminal_activation_toggle = new \OpenAPI\Client\Model\TerminalActivationToggle(); // \OpenAPI\Client\Model\TerminalActivationToggle

try {
    $result = $apiInstance->terminalCommission($terminal_activation_toggle);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TerminalApi->terminalCommission: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **terminal_activation_toggle** | [**\OpenAPI\Client\Model\TerminalActivationToggle**](../Model/TerminalActivationToggle.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\TerminalCommissionDeviceResponse**](../Model/TerminalCommissionDeviceResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `terminalDecommission()`

```php
terminalDecommission($terminal_activation_toggle): \OpenAPI\Client\Model\TerminalDecommissionDeviceResponse
```

Decommission Terminal

Unlink your debug device from your integration

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TerminalApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$terminal_activation_toggle = new \OpenAPI\Client\Model\TerminalActivationToggle(); // \OpenAPI\Client\Model\TerminalActivationToggle

try {
    $result = $apiInstance->terminalDecommission($terminal_activation_toggle);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TerminalApi->terminalDecommission: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **terminal_activation_toggle** | [**\OpenAPI\Client\Model\TerminalActivationToggle**](../Model/TerminalActivationToggle.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\TerminalDecommissionDeviceResponse**](../Model/TerminalDecommissionDeviceResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `terminalFetch()`

```php
terminalFetch($terminal_id): \OpenAPI\Client\Model\TerminalGetResponse
```

Fetch Terminal

Get the details of a Terminal

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TerminalApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$terminal_id = 'terminal_id_example'; // string

try {
    $result = $apiInstance->terminalFetch($terminal_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TerminalApi->terminalFetch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **terminal_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\TerminalGetResponse**](../Model/TerminalGetResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `terminalFetchEventStatus()`

```php
terminalFetchEventStatus($terminal_id, $event_id): \OpenAPI\Client\Model\Response
```

Fetch Event Status

Check the status of an event sent to the Terminal

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TerminalApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$terminal_id = Z0R4orOU; // string
$event_id = 616d721e8c5cd40a0cdd54a6; // string

try {
    $result = $apiInstance->terminalFetchEventStatus($terminal_id, $event_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TerminalApi->terminalFetchEventStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **terminal_id** | **string**|  | |
| **event_id** | **string**|  | |

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

## `terminalFetchTerminalStatus()`

```php
terminalFetchTerminalStatus($terminal_id): \OpenAPI\Client\Model\TerminalGetStatusResponse
```

Fetch Terminal Status

Check the availiability of a Terminal before sending an event to it

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TerminalApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$terminal_id = Z0R4orOU; // string

try {
    $result = $apiInstance->terminalFetchTerminalStatus($terminal_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TerminalApi->terminalFetchTerminalStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **terminal_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\TerminalGetStatusResponse**](../Model/TerminalGetStatusResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `terminalList()`

```php
terminalList($next, $previous, $per_page): \OpenAPI\Client\Model\TerminalListsResponse
```

List Terminals

List the Terminals available on your integration

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TerminalApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$next = 'next_example'; // string
$previous = 'previous_example'; // string
$per_page = 'per_page_example'; // string

try {
    $result = $apiInstance->terminalList($next, $previous, $per_page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TerminalApi->terminalList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **next** | **string**|  | [optional] |
| **previous** | **string**|  | [optional] |
| **per_page** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\TerminalListsResponse**](../Model/TerminalListsResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `terminalSendEvent()`

```php
terminalSendEvent($id, $terminal_send_event): \OpenAPI\Client\Model\Response
```

Send Event

Send an event from your application to the Paystack Terminal

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TerminalApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = Z0R4orOU; // string
$terminal_send_event = new \OpenAPI\Client\Model\TerminalSendEvent(); // \OpenAPI\Client\Model\TerminalSendEvent

try {
    $result = $apiInstance->terminalSendEvent($id, $terminal_send_event);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TerminalApi->terminalSendEvent: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |
| **terminal_send_event** | [**\OpenAPI\Client\Model\TerminalSendEvent**](../Model/TerminalSendEvent.md)|  | [optional] |

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

## `terminalUpdate()`

```php
terminalUpdate($terminal_id, $terminal_upate): \OpenAPI\Client\Model\TerminalUpdateResponse
```

Update Terminal

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TerminalApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$terminal_id = 'terminal_id_example'; // string
$terminal_upate = new \OpenAPI\Client\Model\TerminalUpate(); // \OpenAPI\Client\Model\TerminalUpate

try {
    $result = $apiInstance->terminalUpdate($terminal_id, $terminal_upate);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TerminalApi->terminalUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **terminal_id** | **string**|  | |
| **terminal_upate** | [**\OpenAPI\Client\Model\TerminalUpate**](../Model/TerminalUpate.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\TerminalUpdateResponse**](../Model/TerminalUpdateResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
