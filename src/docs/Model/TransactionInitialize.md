# # TransactionInitialize

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **string** | Customer&#39;s email address |
**amount** | **int** | Amount should be in smallest denomination of the currency. For example if currency is NGN, pesewas, if currency is GHS, and cents, if currency is ZAR |
**currency** | [**\OpenAPI\Client\Model\Currency**](Currency.md) |  | [optional]
**reference** | **string** | Unique transaction reference. Only -, ., &#x3D; and alphanumeric characters allowed. | [optional]
**channels** | **string[]** | An array of payment channels to control what channels you want to make available to the user to make a payment with | [optional]
**callback_url** | **string** | Fully qualified url, e.g. https://example.com/ to redirect your customers to after a successful payment. Use this to override the callback url provided on the dashboard for this transaction | [optional]
**plan** | **string** | If transaction is to create a subscription to a predefined plan, provide plan code here.  This would invalidate the value provided in amount | [optional]
**invoice_limit** | **int** | Number of times to charge customer during subscription to plan | [optional]
**split_code** | **string** | The split code of the transaction split | [optional]
**split** | [**\OpenAPI\Client\Model\SplitCreate**](SplitCreate.md) |  | [optional]
**subaccount** | **string** | The code for the subaccount that owns the payment | [optional]
**transaction_charge** | **string** | A flat fee to charge the subaccount for a transaction.  This overrides the split percentage set when the subaccount was created | [optional]
**bearer** | **string** | The bearer of the transaction charge | [optional]
**label** | **string** | Used to replace the email address shown on the Checkout | [optional]
**metadata** | **string** | Stringified JSON object of custom data | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
