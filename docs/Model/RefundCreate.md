# # RefundCreate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**transaction** | **string** | Transaction reference or id |
**amount** | **int** | Amount ( in kobo if currency is NGN, pesewas, if currency is GHS, and cents, if currency is ZAR ) to be refunded to the customer.  Amount cannot be more than the original transaction amount | [optional]
**currency** | **string** | Three-letter ISO currency. Allowed values are NGN, GHS, ZAR or USD | [optional]
**customer_note** | **string** | Customer reason | [optional]
**merchant_note** | **string** | Merchant reason | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
