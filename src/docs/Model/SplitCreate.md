# # SplitCreate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Name of the transaction split |
**type** | **string** | The type of transaction split you want to create. |
**subaccounts** | [**\OpenAPI\Client\Model\SplitSubaccounts[]**](SplitSubaccounts.md) | A list of object containing subaccount code and number of shares |
**currency** | **string** | The transaction currency |
**bearer_type** | **string** | This allows you specify how the transaction charge should be processed | [optional]
**bearer_subaccount** | **string** | This is the subaccount code of the customer or partner that would bear the transaction charge if you specified subaccount as the bearer type | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
