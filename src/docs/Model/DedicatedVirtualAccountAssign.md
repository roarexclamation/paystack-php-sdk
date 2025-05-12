# # DedicatedVirtualAccountAssign

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **string** | Customer&#39;s email address |
**first_name** | **string** | Customer&#39;s first name |
**last_name** | **string** | Customer&#39;s last name |
**phone** | **string** | Customer&#39;s phone name |
**preferred_bank** | **string** | The bank slug for preferred bank. To get a list of available banks,  use the List Banks endpoint, passing &#x60;pay_with_bank_transfer&#x3D;true&#x60; query parameter |
**country** | **string** | Currently accepts NG only |
**account_number** | **string** | Customer&#39;s account number | [optional]
**bvn** | **string** | Customer&#39;s Bank Verification Number | [optional]
**bank_code** | **string** | Customer&#39;s bank code | [optional]
**subaccount** | **string** | Subaccount code of the account you want to split the transaction with | [optional]
**split_code** | **string** | Split code consisting of the lists of accounts you want to split the transaction with | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
