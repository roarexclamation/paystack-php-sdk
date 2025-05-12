# OpenAPI\Client\TransactionApi

All URIs are relative to https://api.paystack.co, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**transactionChargeAuthorization()**](TransactionApi.md#transactionChargeAuthorization) | **POST** /transaction/charge_authorization | Charge Authorization |
| [**transactionDownload()**](TransactionApi.md#transactionDownload) | **GET** /transaction/export | Export Transactions |
| [**transactionEvent()**](TransactionApi.md#transactionEvent) | **GET** /transaction/{id}/event | Get Transaction Event |
| [**transactionFetch()**](TransactionApi.md#transactionFetch) | **GET** /transaction/{id} | Fetch Transaction |
| [**transactionInitialize()**](TransactionApi.md#transactionInitialize) | **POST** /transaction/initialize | Initialize Transaction |
| [**transactionList()**](TransactionApi.md#transactionList) | **GET** /transaction | List Transactions |
| [**transactionPartialDebit()**](TransactionApi.md#transactionPartialDebit) | **POST** /transaction/partial_debit | Partial Debit |
| [**transactionSession()**](TransactionApi.md#transactionSession) | **GET** /transaction/{id}/session | Get Transaction Session |
| [**transactionTimeline()**](TransactionApi.md#transactionTimeline) | **GET** /transaction/timeline/{id} | Fetch Transaction Timeline |
| [**transactionTotals()**](TransactionApi.md#transactionTotals) | **GET** /transaction/totals | Transaction Totals |
| [**transactionVerify()**](TransactionApi.md#transactionVerify) | **GET** /transaction/verify/{reference} | Verify Transaction |


## `transactionChargeAuthorization()`

```php
transactionChargeAuthorization($transaction_charge_authorization): \OpenAPI\Client\Model\TransactionChargeResponse
```

Charge Authorization

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TransactionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$transaction_charge_authorization = new \OpenAPI\Client\Model\TransactionChargeAuthorization(); // \OpenAPI\Client\Model\TransactionChargeAuthorization

try {
    $result = $apiInstance->transactionChargeAuthorization($transaction_charge_authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionApi->transactionChargeAuthorization: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **transaction_charge_authorization** | [**\OpenAPI\Client\Model\TransactionChargeAuthorization**](../Model/TransactionChargeAuthorization.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\TransactionChargeResponse**](../Model/TransactionChargeResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `transactionDownload()`

```php
transactionDownload($from, $to, $status, $customer, $subaccount_code, $settlement): \OpenAPI\Client\Model\TransactionExportResponse
```

Export Transactions

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TransactionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$from = 2024-06-01T00:00:01Z; // \DateTime | The start date
$to = 2024-06-30T13:36:54Z; // \DateTime | The end date
$status = success; // string | Filter by the status of the transaction
$customer = CUS_eqt26928wowif7z; // string | Filter by customer code
$subaccount_code = ACCT_dskvlw3y3dMukmt; // string | Filter by subaccount code
$settlement = 5687910; // int | Filter by the settlement ID

try {
    $result = $apiInstance->transactionDownload($from, $to, $status, $customer, $subaccount_code, $settlement);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionApi->transactionDownload: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **from** | **\DateTime**| The start date | [optional] |
| **to** | **\DateTime**| The end date | [optional] |
| **status** | **string**| Filter by the status of the transaction | [optional] |
| **customer** | **string**| Filter by customer code | [optional] |
| **subaccount_code** | **string**| Filter by subaccount code | [optional] |
| **settlement** | **int**| Filter by the settlement ID | [optional] |

### Return type

[**\OpenAPI\Client\Model\TransactionExportResponse**](../Model/TransactionExportResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `transactionEvent()`

```php
transactionEvent($id): \OpenAPI\Client\Model\Response
```

Get Transaction Event

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TransactionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 3936799950; // int

try {
    $result = $apiInstance->transactionEvent($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionApi->transactionEvent: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**|  | |

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

## `transactionFetch()`

```php
transactionFetch($id): \OpenAPI\Client\Model\TransactionFetchResponse
```

Fetch Transaction

Fetch a transaction to get its details

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TransactionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The ID of the transaction to fetch

try {
    $result = $apiInstance->transactionFetch($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionApi->transactionFetch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The ID of the transaction to fetch | |

### Return type

[**\OpenAPI\Client\Model\TransactionFetchResponse**](../Model/TransactionFetchResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `transactionInitialize()`

```php
transactionInitialize($transaction_initialize): \OpenAPI\Client\Model\TransactionInitializeResponse
```

Initialize Transaction

Create a new transaction

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TransactionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$transaction_initialize = new \OpenAPI\Client\Model\TransactionInitialize(); // \OpenAPI\Client\Model\TransactionInitialize

try {
    $result = $apiInstance->transactionInitialize($transaction_initialize);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionApi->transactionInitialize: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **transaction_initialize** | [**\OpenAPI\Client\Model\TransactionInitialize**](../Model/TransactionInitialize.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\TransactionInitializeResponse**](../Model/TransactionInitializeResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `transactionList()`

```php
transactionList($use_cursor, $next, $previous, $per_page, $page, $from, $to, $channel, $terminal_id, $customer_code, $amount, $status, $source, $subaccount_code, $split_code, $settlement): \OpenAPI\Client\Model\TransactionListResponse
```

List Transactions

List transactions that has occurred on your integration

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TransactionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$use_cursor = True; // bool | A flag to indicate if cursor based pagination should be used
$next = 'next_example'; // string | An alphanumeric value returned for every cursor based retrieval, used to retrieve the next set of data
$previous = 'previous_example'; // string | An alphanumeric value returned for every cursor based retrieval, used to retrieve the previous set of data
$per_page = 56; // int | The number of records to fetch per request
$page = 56; // int | Used to indicate the offeset to retrieve data from
$from = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | The start date
$to = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | The end date
$channel = 'channel_example'; // string | The payment method the customer used to complete the transaction
$terminal_id = 'terminal_id_example'; // string | The terminal ID to filter all transactions from a terminal
$customer_code = 'customer_code_example'; // string | The customer code to filter all transactions from a customer
$amount = 56; // int | Filter transactions by a certain amount
$status = 'status_example'; // string | Filter transaction by status
$source = 'source_example'; // string | The origin of the payment
$subaccount_code = 'subaccount_code_example'; // string | Filter transaction by subaccount code
$split_code = 'split_code_example'; // string | Filter transaction by split code
$settlement = 56; // int | The settlement ID to filter for settled transactions

try {
    $result = $apiInstance->transactionList($use_cursor, $next, $previous, $per_page, $page, $from, $to, $channel, $terminal_id, $customer_code, $amount, $status, $source, $subaccount_code, $split_code, $settlement);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionApi->transactionList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **use_cursor** | **bool**| A flag to indicate if cursor based pagination should be used | [optional] |
| **next** | **string**| An alphanumeric value returned for every cursor based retrieval, used to retrieve the next set of data | [optional] |
| **previous** | **string**| An alphanumeric value returned for every cursor based retrieval, used to retrieve the previous set of data | [optional] |
| **per_page** | **int**| The number of records to fetch per request | [optional] |
| **page** | **int**| Used to indicate the offeset to retrieve data from | [optional] |
| **from** | **\DateTime**| The start date | [optional] |
| **to** | **\DateTime**| The end date | [optional] |
| **channel** | **string**| The payment method the customer used to complete the transaction | [optional] |
| **terminal_id** | **string**| The terminal ID to filter all transactions from a terminal | [optional] |
| **customer_code** | **string**| The customer code to filter all transactions from a customer | [optional] |
| **amount** | **int**| Filter transactions by a certain amount | [optional] |
| **status** | **string**| Filter transaction by status | [optional] |
| **source** | **string**| The origin of the payment | [optional] |
| **subaccount_code** | **string**| Filter transaction by subaccount code | [optional] |
| **split_code** | **string**| Filter transaction by split code | [optional] |
| **settlement** | **int**| The settlement ID to filter for settled transactions | [optional] |

### Return type

[**\OpenAPI\Client\Model\TransactionListResponse**](../Model/TransactionListResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `transactionPartialDebit()`

```php
transactionPartialDebit($transaction_partial_debit): \OpenAPI\Client\Model\TransactionPartialDebitResponse
```

Partial Debit

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TransactionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$transaction_partial_debit = new \OpenAPI\Client\Model\TransactionPartialDebit(); // \OpenAPI\Client\Model\TransactionPartialDebit

try {
    $result = $apiInstance->transactionPartialDebit($transaction_partial_debit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionApi->transactionPartialDebit: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **transaction_partial_debit** | [**\OpenAPI\Client\Model\TransactionPartialDebit**](../Model/TransactionPartialDebit.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\TransactionPartialDebitResponse**](../Model/TransactionPartialDebitResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `transactionSession()`

```php
transactionSession($id): \OpenAPI\Client\Model\Response
```

Get Transaction Session

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TransactionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 3936799950; // int

try {
    $result = $apiInstance->transactionSession($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionApi->transactionSession: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**|  | |

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

## `transactionTimeline()`

```php
transactionTimeline($id): \OpenAPI\Client\Model\TransactionTimelineResponse
```

Fetch Transaction Timeline

Get the details about the lifecycle of a transaction from initiation to completion

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TransactionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 3936799950; // int

try {
    $result = $apiInstance->transactionTimeline($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionApi->transactionTimeline: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**|  | |

### Return type

[**\OpenAPI\Client\Model\TransactionTimelineResponse**](../Model/TransactionTimelineResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `transactionTotals()`

```php
transactionTotals($from, $to): \OpenAPI\Client\Model\TransactionTotalsResponse
```

Transaction Totals

Get the total amount of all transactions

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TransactionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$from = 2024-06-01T00:00:01Z; // \DateTime | The start date
$to = 2024-06-30T13:36:54Z; // \DateTime | The end date

try {
    $result = $apiInstance->transactionTotals($from, $to);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionApi->transactionTotals: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **from** | **\DateTime**| The start date | [optional] |
| **to** | **\DateTime**| The end date | [optional] |

### Return type

[**\OpenAPI\Client\Model\TransactionTotalsResponse**](../Model/TransactionTotalsResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `transactionVerify()`

```php
transactionVerify($reference): \OpenAPI\Client\Model\TransactionVerifyResponse
```

Verify Transaction

Verify a previously initiated transaction using it's reference

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TransactionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$reference = 'reference_example'; // string | The transaction reference to verify

try {
    $result = $apiInstance->transactionVerify($reference);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionApi->transactionVerify: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **reference** | **string**| The transaction reference to verify | |

### Return type

[**\OpenAPI\Client\Model\TransactionVerifyResponse**](../Model/TransactionVerifyResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
