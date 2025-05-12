# # SubscriptionCreate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**customer** | **string** | Customer&#39;s email address or customer code |
**plan** | **string** | Plan code |
**authorization** | **string** | If customer has multiple authorizations, you can set the desired authorization you wish to use for this subscription here.  If this is not supplied, the customer&#39;s most recent authorization would be used | [optional]
**start_date** | **\DateTime** | Set the date for the first debit. (ISO 8601 format) e.g. 2017-05-16T00:30:13+01:00 | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
