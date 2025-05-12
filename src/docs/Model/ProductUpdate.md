# # ProductUpdate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Name of product | [optional]
**description** | **string** | The description of the product | [optional]
**price** | **int** | Price should be in kobo if currency is NGN, pesewas, if currency is GHS, and cents, if currency is ZAR | [optional]
**currency** | **string** | Currency in which price is set. Allowed values are: NGN, GHS, ZAR or USD | [optional]
**unlimited** | **bool** | Set to true if the product has unlimited stock. Leave as false if the product has limited stock | [optional]
**quantity** | **int** | Number of products in stock. Use if limited is true | [optional]
**split_code** | **string** | The split code if sharing the transaction with partners | [optional]
**metadata** | **string** | Stringified JSON object of custom data | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
