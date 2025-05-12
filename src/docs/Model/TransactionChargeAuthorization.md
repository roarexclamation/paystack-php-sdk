# # TransactionChargeAuthorization

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **string** | Customer&#39;s email address |
**amount** | **int** | Amount in the lower denomination of your currency |
**authorization_code** | **string** | Valid authorization code to charge |
**reference** | **string** | Unique transaction reference. Only -, ., &#x3D; and alphanumeric characters allowed. | [optional]
**currency** | [**\OpenAPI\Client\Model\Currency**](Currency.md) |  | [optional]
**split_code** | **string** | The split code of the transaction split | [optional]
**subaccount** | **string** | The code for the subaccount that owns the payment | [optional]
**transaction_charge** | **string** | A flat fee to charge the subaccount for a transaction.  This overrides the split percentage set when the subaccount was created | [optional]
**bearer** | **string** | The bearer of the transaction charge | [optional]
**metadata** | **string** | Stringified JSON object of custom data | [optional]
**queue** | **bool** | If you are making a scheduled charge call, it is a good idea to queue them so the processing system does not get overloaded causing transaction processing errors. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
