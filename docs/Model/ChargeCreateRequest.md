# # ChargeCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **string** | Customer&#39;s email address |
**amount** | **string** | Amount should be in kobo if currency is NGN, pesewas, if currency is GHS, and cents, if currency is ZAR |
**authorization_code** | **string** | An authorization code to charge. | [optional]
**pin** | **string** | 4-digit PIN (send with a non-reusable authorization code) | [optional]
**reference** | **string** | Unique transaction reference. Only -, .&#x60;, &#x3D; and alphanumeric characters allowed. | [optional]
**birthday** | **\DateTime** | The customer&#39;s birthday in the format YYYY-MM-DD e.g 2017-05-16 | [optional]
**device_id** | **string** | This is the unique identifier of the device a user uses in making payment.  Only -, .&#x60;, &#x3D; and alphanumeric characters are allowed. | [optional]
**metadata** | **string** | Stringified JSON object of custom data | [optional]
**bank** | [**\OpenAPI\Client\Model\Bank**](Bank.md) |  | [optional]
**mobile_money** | [**\OpenAPI\Client\Model\MobileMoney**](MobileMoney.md) |  | [optional]
**ussd** | [**\OpenAPI\Client\Model\USSD**](USSD.md) |  | [optional]
**eft** | [**\OpenAPI\Client\Model\EFT**](EFT.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
