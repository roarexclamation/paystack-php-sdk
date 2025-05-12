# # TransactionPartialDebit

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **string** | Customer&#39;s email address |
**amount** | **int** | Specified in the lowest denomination of your currency |
**authorization_code** | **string** | Valid authorization code to charge |
**currency** | [**\OpenAPI\Client\Model\Currency**](Currency.md) |  |
**at_least** | **string** | Minimum amount to charge | [optional]
**reference** | **string** | Unique transaction reference. Only -, ., &#x3D; and alphanumeric characters allowed. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
