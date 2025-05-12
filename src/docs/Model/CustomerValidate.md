# # CustomerValidate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**first_name** | **string** | Customer&#39;s first name |
**middle_name** | **string** | Customer&#39;s middle name | [optional]
**last_name** | **string** | Customer&#39;s last name |
**type** | **string** | Predefined types of identification. |
**value** | **string** | Customer&#39;s identification number. Required if type is bvn | [optional]
**country** | **string** | Two-letter country code of identification issuer |
**bvn** | **string** | Customer&#39;s Bank Verification Number |
**bank_code** | **string** | You can get the list of bank codes by calling the List Banks endpoint (https://api.paystack.co/bank). |
**account_number** | **string** | Customer&#39;s bank account number. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
