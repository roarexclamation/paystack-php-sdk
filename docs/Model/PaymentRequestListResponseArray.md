# # PaymentRequestListResponseArray

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  |
**integration** | **int** |  |
**domain** | **string** |  |
**amount** | **int** |  |
**currency** | **string** |  |
**due_date** | **string** |  |
**has_invoice** | **bool** |  |
**invoice_number** | **int** |  |
**description** | **string** |  |
**pdf_url** | **string** |  |
**line_items** | [**\OpenAPI\Client\Model\PaymentRequestLineItemsArray[]**](PaymentRequestLineItemsArray.md) |  |
**tax** | [**\OpenAPI\Client\Model\PaymentRequestTaxArray[]**](PaymentRequestTaxArray.md) |  |
**request_code** | **string** |  |
**status** | **string** |  |
**paid** | **bool** |  |
**paid_at** | **mixed** |  |
**metadata** | **mixed** |  |
**notifications** | **mixed[]** |  |
**offline_reference** | **string** |  |
**customer** | [**\OpenAPI\Client\Model\TransactionFetchResponseDataCustomer**](TransactionFetchResponseDataCustomer.md) |  |
**created_at** | **string** |  |
**discount** | **mixed** |  |
**split_code** | **string** |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
