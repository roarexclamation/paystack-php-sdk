# # PaymentRequestFinalizeResponseData

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
**pdf_url** | **mixed** |  |
**line_items** | [**\OpenAPI\Client\Model\PaymentRequestLineItemsArray[]**](PaymentRequestLineItemsArray.md) |  |
**tax** | [**\OpenAPI\Client\Model\PaymentRequestTaxArray[]**](PaymentRequestTaxArray.md) |  |
**request_code** | **string** |  |
**status** | **string** |  |
**paid** | **bool** |  |
**paid_at** | **mixed** |  |
**metadata** | **mixed** |  |
**notifications** | **mixed[]** |  |
**offline_reference** | **string** |  |
**customer** | [**\OpenAPI\Client\Model\PaymentRequestUpdateResponseDataCustomer**](PaymentRequestUpdateResponseDataCustomer.md) |  |
**created_at** | **string** |  |
**discount** | [**\OpenAPI\Client\Model\PaymentRequestFinalizeResponseDataDiscount**](PaymentRequestFinalizeResponseDataDiscount.md) |  |
**split_code** | **mixed** |  |
**pending_amount** | **int** |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
