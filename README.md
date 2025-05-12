# OpenAPIClient-php

The OpenAPI specification of the Paystack API that merchants and developers can harness to build financial solutions in Africa.

## Installation & Usage

### Requirements

PHP 8.1 and later.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```bash
composer require roar-exclamation/paysatck-php-sdk
```

Then run `composer install`

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ApplePayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$use_cursor = True; // bool
$next = 'next_example'; // string
$previous = 'previous_example'; // string

try {
    $result = $apiInstance->applePayListDomain($use_cursor, $next, $previous);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplePayApi->applePayListDomain: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *https://api.paystack.co*

| Class                        | Method                                                                                                              | HTTP request                                     | Description                                         |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------ | --------------------------------------------------- |
| _ApplePayApi_                | [**applePayListDomain**](docs/Api/ApplePayApi.md#applepaylistdomain)                                                | **GET** /apple-pay/domain                        | List Domains                                        |
| _ApplePayApi_                | [**applePayRegisterDomain**](docs/Api/ApplePayApi.md#applepayregisterdomain)                                        | **POST** /apple-pay/domain                       | Register Domain                                     |
| _ApplePayApi_                | [**applePayUnregisterDomain**](docs/Api/ApplePayApi.md#applepayunregisterdomain)                                    | **DELETE** /apple-pay/domain                     | Unregister Domain                                   |
| _BalanceApi_                 | [**balanceFetch**](docs/Api/BalanceApi.md#balancefetch)                                                             | **GET** /balance                                 | Fetch Balance                                       |
| _BalanceApi_                 | [**balanceLedger**](docs/Api/BalanceApi.md#balanceledger)                                                           | **GET** /balance/ledger                          | Balance Ledger                                      |
| _BankApi_                    | [**bankList**](docs/Api/BankApi.md#banklist)                                                                        | **GET** /bank                                    | List Banks                                          |
| _BankApi_                    | [**bankResolveAccountNumber**](docs/Api/BankApi.md#bankresolveaccountnumber)                                        | **GET** /bank/resolve                            | Resolve Account Number                              |
| _BankApi_                    | [**bankValidateAccountNumber**](docs/Api/BankApi.md#bankvalidateaccountnumber)                                      | **POST** /bank/validate                          | Validate Bank Account                               |
| _BulkChargeApi_              | [**bulkChargeCharges**](docs/Api/BulkChargeApi.md#bulkchargecharges)                                                | **GET** /bulkcharge/{code}/charges               | Fetch Charges in a Batch                            |
| _BulkChargeApi_              | [**bulkChargeFetch**](docs/Api/BulkChargeApi.md#bulkchargefetch)                                                    | **GET** /bulkcharge/{code}                       | Fetch Bulk Charge Batch                             |
| _BulkChargeApi_              | [**bulkChargeInitiate**](docs/Api/BulkChargeApi.md#bulkchargeinitiate)                                              | **POST** /bulkcharge                             | Initiate Bulk Charge                                |
| _BulkChargeApi_              | [**bulkChargeList**](docs/Api/BulkChargeApi.md#bulkchargelist)                                                      | **GET** /bulkcharge                              | List Bulk Charge Batches                            |
| _BulkChargeApi_              | [**bulkChargePause**](docs/Api/BulkChargeApi.md#bulkchargepause)                                                    | **GET** /bulkcharge/pause/{code}                 | Pause Bulk Charge Batch                             |
| _BulkChargeApi_              | [**bulkChargeResume**](docs/Api/BulkChargeApi.md#bulkchargeresume)                                                  | **GET** /bulkcharge/resume/{code}                | Resume Bulk Charge Batch                            |
| _ChargeApi_                  | [**chargeCheck**](docs/Api/ChargeApi.md#chargecheck)                                                                | **GET** /charge/{reference}                      | Check pending charge                                |
| _ChargeApi_                  | [**chargeCreate**](docs/Api/ChargeApi.md#chargecreate)                                                              | **POST** /charge                                 | Create Charge                                       |
| _ChargeApi_                  | [**chargeSubmitAddress**](docs/Api/ChargeApi.md#chargesubmitaddress)                                                | **POST** /charge/submit_address                  | Submit Address                                      |
| _ChargeApi_                  | [**chargeSubmitBirthday**](docs/Api/ChargeApi.md#chargesubmitbirthday)                                              | **POST** /charge/submit_birthday                 | Submit Birthday                                     |
| _ChargeApi_                  | [**chargeSubmitOtp**](docs/Api/ChargeApi.md#chargesubmitotp)                                                        | **POST** /charge/submit_otp                      | Submit OTP                                          |
| _ChargeApi_                  | [**chargeSubmitPhone**](docs/Api/ChargeApi.md#chargesubmitphone)                                                    | **POST** /charge/submit_phone                    | Submit Phone                                        |
| _ChargeApi_                  | [**chargeSubmitPin**](docs/Api/ChargeApi.md#chargesubmitpin)                                                        | **POST** /charge/submit_pin                      | Submit PIN                                          |
| _CustomerApi_                | [**customerCreate**](docs/Api/CustomerApi.md#customercreate)                                                        | **POST** /customer                               | Create Customer                                     |
| _CustomerApi_                | [**customerDeactivateAuthorization**](docs/Api/CustomerApi.md#customerdeactivateauthorization)                      | **POST** /customer/deactivate_authorization      | Deactivate Authorization                            |
| _CustomerApi_                | [**customerFetch**](docs/Api/CustomerApi.md#customerfetch)                                                          | **GET** /customer/{code}                         | Fetch Customer                                      |
| _CustomerApi_                | [**customerList**](docs/Api/CustomerApi.md#customerlist)                                                            | **GET** /customer                                | List Customers                                      |
| _CustomerApi_                | [**customerRiskAction**](docs/Api/CustomerApi.md#customerriskaction)                                                | **POST** /customer/set_risk_action               | White/blacklist Customer                            |
| _CustomerApi_                | [**customerUpdate**](docs/Api/CustomerApi.md#customerupdate)                                                        | **PUT** /customer/{code}                         | Update Customer                                     |
| _CustomerApi_                | [**customerValidate**](docs/Api/CustomerApi.md#customervalidate)                                                    | **POST** /customer/{code}/identification         | Validate Customer                                   |
| _DedicatedVirtualAccountApi_ | [**dedicatedAccountAddSplit**](docs/Api/DedicatedVirtualAccountApi.md#dedicatedaccountaddsplit)                     | **POST** /dedicated_account/split                | Split Dedicated Account Transaction                 |
| _DedicatedVirtualAccountApi_ | [**dedicatedAccountAssign**](docs/Api/DedicatedVirtualAccountApi.md#dedicatedaccountassign)                         | **POST** /dedicated_account/assign               | Assign Dedicated Account                            |
| _DedicatedVirtualAccountApi_ | [**dedicatedAccountAvailableProviders**](docs/Api/DedicatedVirtualAccountApi.md#dedicatedaccountavailableproviders) | **GET** /dedicated_account/available_providers   | Fetch Bank Providers                                |
| _DedicatedVirtualAccountApi_ | [**dedicatedAccountCreate**](docs/Api/DedicatedVirtualAccountApi.md#dedicatedaccountcreate)                         | **POST** /dedicated_account                      | Create Dedicated Account                            |
| _DedicatedVirtualAccountApi_ | [**dedicatedAccountDeactivate**](docs/Api/DedicatedVirtualAccountApi.md#dedicatedaccountdeactivate)                 | **DELETE** /dedicated_account/{account_id}       | Deactivate Dedicated Account                        |
| _DedicatedVirtualAccountApi_ | [**dedicatedAccountFetch**](docs/Api/DedicatedVirtualAccountApi.md#dedicatedaccountfetch)                           | **GET** /dedicated_account/{account_id}          | Fetch Dedicated Account                             |
| _DedicatedVirtualAccountApi_ | [**dedicatedAccountList**](docs/Api/DedicatedVirtualAccountApi.md#dedicatedaccountlist)                             | **GET** /dedicated_account                       | List Dedicated Accounts                             |
| _DedicatedVirtualAccountApi_ | [**dedicatedAccountRemoveSplit**](docs/Api/DedicatedVirtualAccountApi.md#dedicatedaccountremovesplit)               | **DELETE** /dedicated_account/split              | Remove Split from Dedicated Account                 |
| _DedicatedVirtualAccountApi_ | [**dedicatedAccountRequery**](docs/Api/DedicatedVirtualAccountApi.md#dedicatedaccountrequery)                       | **GET** /dedicated_account/requery               | Requery Dedicated Account                           |
| _DisputeApi_                 | [**disputeDownload**](docs/Api/DisputeApi.md#disputedownload)                                                       | **GET** /dispute/export                          | Export Disputes                                     |
| _DisputeApi_                 | [**disputeEvidence**](docs/Api/DisputeApi.md#disputeevidence)                                                       | **POST** /dispute/{id}/evidence                  | Add Evidence                                        |
| _DisputeApi_                 | [**disputeFetch**](docs/Api/DisputeApi.md#disputefetch)                                                             | **GET** /dispute/{id}                            | Fetch Dispute                                       |
| _DisputeApi_                 | [**disputeList**](docs/Api/DisputeApi.md#disputelist)                                                               | **GET** /dispute                                 | List Disputes                                       |
| _DisputeApi_                 | [**disputeResolve**](docs/Api/DisputeApi.md#disputeresolve)                                                         | **PUT** /dispute/{id}/resolve                    | Resolve a Dispute                                   |
| _DisputeApi_                 | [**disputeTransaction**](docs/Api/DisputeApi.md#disputetransaction)                                                 | **GET** /dispute/transaction/{id}                | List Transaction Disputes                           |
| _DisputeApi_                 | [**disputeUpdate**](docs/Api/DisputeApi.md#disputeupdate)                                                           | **PUT** /dispute/{id}                            | Update Dispute                                      |
| _DisputeApi_                 | [**disputeUploadUrl**](docs/Api/DisputeApi.md#disputeuploadurl)                                                     | **GET** /dispute/{id}/upload_url                 | Get Upload URL                                      |
| _IntegrationApi_             | [**integrationFetchPaymentSessionTimeout**](docs/Api/IntegrationApi.md#integrationfetchpaymentsessiontimeout)       | **GET** /integration/payment_session_timeout     | Fetch Payment Session Timeout                       |
| _IntegrationApi_             | [**integrationUpdatePaymentSessionTimeout**](docs/Api/IntegrationApi.md#integrationupdatepaymentsessiontimeout)     | **PUT** /integration/payment_session_timeout     | Update Payment Session Timeout                      |
| _MiscellaneousApi_           | [**miscellaneousAvs**](docs/Api/MiscellaneousApi.md#miscellaneousavs)                                               | **GET** /address_verification/states             | List States (AVS)                                   |
| _MiscellaneousApi_           | [**miscellaneousListCountries**](docs/Api/MiscellaneousApi.md#miscellaneouslistcountries)                           | **GET** /country                                 | List Countries                                      |
| _MiscellaneousApi_           | [**miscellaneousResolveCardBin**](docs/Api/MiscellaneousApi.md#miscellaneousresolvecardbin)                         | **GET** /decision/bin/{bin}                      | Resolve Card BIN                                    |
| _OrderApi_                   | [**orderCreate**](docs/Api/OrderApi.md#ordercreate)                                                                 | **POST** /order                                  | Create Order                                        |
| _OrderApi_                   | [**orderFetch**](docs/Api/OrderApi.md#orderfetch)                                                                   | **GET** /order/{id}                              | Fetch Order                                         |
| _OrderApi_                   | [**orderFetchProducts**](docs/Api/OrderApi.md#orderfetchproducts)                                                   | **GET** /order/product/{id}                      | Fetch Products Order                                |
| _OrderApi_                   | [**orderList**](docs/Api/OrderApi.md#orderlist)                                                                     | **GET** /order                                   | List Orders                                         |
| _OrderApi_                   | [**orderValidatePayForMe**](docs/Api/OrderApi.md#ordervalidatepayforme)                                             | **GET** /order/{code}/validate                   | Validate pay for me order                           |
| _PageApi_                    | [**pageAddProducts**](docs/Api/PageApi.md#pageaddproducts)                                                          | **POST** /page/{id}/product                      | Add Products                                        |
| _PageApi_                    | [**pageCheckSlugAvailability**](docs/Api/PageApi.md#pagecheckslugavailability)                                      | **GET** /page/check_slug_availability/{slug}     | Check Slug Availability                             |
| _PageApi_                    | [**pageCreate**](docs/Api/PageApi.md#pagecreate)                                                                    | **POST** /page                                   | Create Page                                         |
| _PageApi_                    | [**pageFetch**](docs/Api/PageApi.md#pagefetch)                                                                      | **GET** /page/{id}                               | Fetch Page                                          |
| _PageApi_                    | [**pageList**](docs/Api/PageApi.md#pagelist)                                                                        | **GET** /page                                    | List Pages                                          |
| _PageApi_                    | [**pageUpdate**](docs/Api/PageApi.md#pageupdate)                                                                    | **PUT** /page/{id}                               | Update Page                                         |
| _PaymentRequestApi_          | [**paymentRequestArchive**](docs/Api/PaymentRequestApi.md#paymentrequestarchive)                                    | **POST** /paymentrequest/archive/{id}            | Archive Payment Request                             |
| _PaymentRequestApi_          | [**paymentRequestCreate**](docs/Api/PaymentRequestApi.md#paymentrequestcreate)                                      | **POST** /paymentrequest                         | Create Payment Request                              |
| _PaymentRequestApi_          | [**paymentRequestFetch**](docs/Api/PaymentRequestApi.md#paymentrequestfetch)                                        | **GET** /paymentrequest/{id}                     | Fetch Payment Request                               |
| _PaymentRequestApi_          | [**paymentRequestFinalize**](docs/Api/PaymentRequestApi.md#paymentrequestfinalize)                                  | **POST** /paymentrequest/finalize/{id}           | Finalize Payment Request                            |
| _PaymentRequestApi_          | [**paymentRequestList**](docs/Api/PaymentRequestApi.md#paymentrequestlist)                                          | **GET** /paymentrequest                          | List Payment Request                                |
| _PaymentRequestApi_          | [**paymentRequestNotify**](docs/Api/PaymentRequestApi.md#paymentrequestnotify)                                      | **POST** /paymentrequest/notify/{id}             | Send Notification                                   |
| _PaymentRequestApi_          | [**paymentRequestTotals**](docs/Api/PaymentRequestApi.md#paymentrequesttotals)                                      | **GET** /paymentrequest/totals                   | Payment Request Total                               |
| _PaymentRequestApi_          | [**paymentRequestUpdate**](docs/Api/PaymentRequestApi.md#paymentrequestupdate)                                      | **PUT** /paymentrequest/{id}                     | Update Payment Request                              |
| _PaymentRequestApi_          | [**paymentRequestVerify**](docs/Api/PaymentRequestApi.md#paymentrequestverify)                                      | **GET** /paymentrequest/verify/{id}              | Verify Payment Request                              |
| _PlanApi_                    | [**planCreate**](docs/Api/PlanApi.md#plancreate)                                                                    | **POST** /plan                                   | Create Plan                                         |
| _PlanApi_                    | [**planFetch**](docs/Api/PlanApi.md#planfetch)                                                                      | **GET** /plan/{code}                             | Fetch Plan                                          |
| _PlanApi_                    | [**planList**](docs/Api/PlanApi.md#planlist)                                                                        | **GET** /plan                                    | List Plans                                          |
| _PlanApi_                    | [**planUpdate**](docs/Api/PlanApi.md#planupdate)                                                                    | **PUT** /plan/{code}                             | Update Plan                                         |
| _ProductApi_                 | [**productCreate**](docs/Api/ProductApi.md#productcreate)                                                           | **POST** /product                                | Create Product                                      |
| _ProductApi_                 | [**productDelete**](docs/Api/ProductApi.md#productdelete)                                                           | **DELETE** /product/{id}                         | Delete Product                                      |
| _ProductApi_                 | [**productFetch**](docs/Api/ProductApi.md#productfetch)                                                             | **GET** /product/{id}                            | Fetch Product                                       |
| _ProductApi_                 | [**productList**](docs/Api/ProductApi.md#productlist)                                                               | **GET** /product                                 | List Products                                       |
| _ProductApi_                 | [**productUpdate**](docs/Api/ProductApi.md#productupdate)                                                           | **PUT** /product/{id}                            | Update product                                      |
| _RefundApi_                  | [**refundCreate**](docs/Api/RefundApi.md#refundcreate)                                                              | **POST** /refund                                 | Create Refund                                       |
| _RefundApi_                  | [**refundFetch**](docs/Api/RefundApi.md#refundfetch)                                                                | **GET** /refund/{id}                             | Fetch Refund                                        |
| _RefundApi_                  | [**refundList**](docs/Api/RefundApi.md#refundlist)                                                                  | **GET** /refund                                  | List Refunds                                        |
| _SettlementApi_              | [**settlementsFetch**](docs/Api/SettlementApi.md#settlementsfetch)                                                  | **GET** /settlement                              | Fetch Settlements                                   |
| _SettlementApi_              | [**settlementsTransaction**](docs/Api/SettlementApi.md#settlementstransaction)                                      | **GET** /settlement/{id}/transaction             | Settlement Transactions                             |
| _SplitApi_                   | [**splitAddSubaccount**](docs/Api/SplitApi.md#splitaddsubaccount)                                                   | **POST** /split/{id}/subaccount/add              | Add Subaccount to Split                             |
| _SplitApi_                   | [**splitCreate**](docs/Api/SplitApi.md#splitcreate)                                                                 | **POST** /split                                  | Create Split                                        |
| _SplitApi_                   | [**splitFetch**](docs/Api/SplitApi.md#splitfetch)                                                                   | **GET** /split/{id}                              | Fetch Split                                         |
| _SplitApi_                   | [**splitList**](docs/Api/SplitApi.md#splitlist)                                                                     | **GET** /split                                   | List/Search Splits                                  |
| _SplitApi_                   | [**splitRemoveSubaccount**](docs/Api/SplitApi.md#splitremovesubaccount)                                             | **POST** /split/{id}/subaccount/remove           | Remove Subaccount from split                        |
| _SplitApi_                   | [**splitUpdate**](docs/Api/SplitApi.md#splitupdate)                                                                 | **PUT** /split/{id}                              | Update Split                                        |
| _StorefrontApi_              | [**storefrontAddProducts**](docs/Api/StorefrontApi.md#storefrontaddproducts)                                        | **POST** /storefront/{id}/product                | Add Products to Storefront                          |
| _StorefrontApi_              | [**storefrontCreate**](docs/Api/StorefrontApi.md#storefrontcreate)                                                  | **POST** /storefront                             | Create Storefront                                   |
| _StorefrontApi_              | [**storefrontDelete**](docs/Api/StorefrontApi.md#storefrontdelete)                                                  | **DELETE** /storefront/{id}                      | Delete Storefront                                   |
| _StorefrontApi_              | [**storefrontDuplicate**](docs/Api/StorefrontApi.md#storefrontduplicate)                                            | **POST** /storefront/{id}/duplicate              | Duplicate Storefront                                |
| _StorefrontApi_              | [**storefrontFetch**](docs/Api/StorefrontApi.md#storefrontfetch)                                                    | **GET** /storefront/{id}                         | Fetch Storefront                                    |
| _StorefrontApi_              | [**storefrontFetchOrders**](docs/Api/StorefrontApi.md#storefrontfetchorders)                                        | **GET** /storefront/{id}/order                   | Fetch Storefront Orders                             |
| _StorefrontApi_              | [**storefrontList**](docs/Api/StorefrontApi.md#storefrontlist)                                                      | **GET** /storefront                              | List Storefronts                                    |
| _StorefrontApi_              | [**storefrontListProducts**](docs/Api/StorefrontApi.md#storefrontlistproducts)                                      | **GET** /storefront/{id}/product                 | List Products in Storefront                         |
| _StorefrontApi_              | [**storefrontPublish**](docs/Api/StorefrontApi.md#storefrontpublish)                                                | **POST** /storefront/{id}/publish                | Publish Storefront                                  |
| _StorefrontApi_              | [**storefrontUpdate**](docs/Api/StorefrontApi.md#storefrontupdate)                                                  | **PUT** /storefront/{id}                         | Update Storefront                                   |
| _StorefrontApi_              | [**storefrontVerifySlug**](docs/Api/StorefrontApi.md#storefrontverifyslug)                                          | **GET** /storefront/verify/{slug}                | Verify Storefront Slug                              |
| _SubaccountApi_              | [**subaccountCreate**](docs/Api/SubaccountApi.md#subaccountcreate)                                                  | **POST** /subaccount                             | Create Subaccount                                   |
| _SubaccountApi_              | [**subaccountFetch**](docs/Api/SubaccountApi.md#subaccountfetch)                                                    | **GET** /subaccount/{code}                       | Fetch Subaccount                                    |
| _SubaccountApi_              | [**subaccountList**](docs/Api/SubaccountApi.md#subaccountlist)                                                      | **GET** /subaccount                              | List Subaccounts                                    |
| _SubaccountApi_              | [**subaccountUpdate**](docs/Api/SubaccountApi.md#subaccountupdate)                                                  | **PUT** /subaccount/{code}                       | Update Subaccount                                   |
| _SubscriptionApi_            | [**subscriptionCreate**](docs/Api/SubscriptionApi.md#subscriptioncreate)                                            | **POST** /subscription                           | Create Subscription                                 |
| _SubscriptionApi_            | [**subscriptionDisable**](docs/Api/SubscriptionApi.md#subscriptiondisable)                                          | **POST** /subscription/disable                   | Disable Subscription                                |
| _SubscriptionApi_            | [**subscriptionEnable**](docs/Api/SubscriptionApi.md#subscriptionenable)                                            | **POST** /subscription/enable                    | Enable Subscription                                 |
| _SubscriptionApi_            | [**subscriptionFetch**](docs/Api/SubscriptionApi.md#subscriptionfetch)                                              | **GET** /subscription/{code}                     | Fetch Subscription                                  |
| _SubscriptionApi_            | [**subscriptionList**](docs/Api/SubscriptionApi.md#subscriptionlist)                                                | **GET** /subscription                            | List Subscriptions                                  |
| _SubscriptionApi_            | [**subscriptionManageEmail**](docs/Api/SubscriptionApi.md#subscriptionmanageemail)                                  | **POST** /subscription/{code}/manage/email       | Send Update Subscription Link                       |
| _SubscriptionApi_            | [**subscriptionManageLink**](docs/Api/SubscriptionApi.md#subscriptionmanagelink)                                    | **GET** /subscription/{code}/manage/link         | Generate Update Subscription Link                   |
| _TerminalApi_                | [**terminalCommission**](docs/Api/TerminalApi.md#terminalcommission)                                                | **POST** /terminal/commission_device             | Commission Terminal                                 |
| _TerminalApi_                | [**terminalDecommission**](docs/Api/TerminalApi.md#terminaldecommission)                                            | **POST** /terminal/decommission_device           | Decommission Terminal                               |
| _TerminalApi_                | [**terminalFetch**](docs/Api/TerminalApi.md#terminalfetch)                                                          | **GET** /terminal/{terminal_id}                  | Fetch Terminal                                      |
| _TerminalApi_                | [**terminalFetchEventStatus**](docs/Api/TerminalApi.md#terminalfetcheventstatus)                                    | **GET** /terminal/{terminal_id}/event/{event_id} | Fetch Event Status                                  |
| _TerminalApi_                | [**terminalFetchTerminalStatus**](docs/Api/TerminalApi.md#terminalfetchterminalstatus)                              | **GET** /terminal/{terminal_id}/presence         | Fetch Terminal Status                               |
| _TerminalApi_                | [**terminalList**](docs/Api/TerminalApi.md#terminallist)                                                            | **GET** /terminal                                | List Terminals                                      |
| _TerminalApi_                | [**terminalSendEvent**](docs/Api/TerminalApi.md#terminalsendevent)                                                  | **POST** /terminal/{id}/event                    | Send Event                                          |
| _TerminalApi_                | [**terminalUpdate**](docs/Api/TerminalApi.md#terminalupdate)                                                        | **PUT** /terminal/{terminal_id}                  | Update Terminal                                     |
| _TransactionApi_             | [**transactionChargeAuthorization**](docs/Api/TransactionApi.md#transactionchargeauthorization)                     | **POST** /transaction/charge_authorization       | Charge Authorization                                |
| _TransactionApi_             | [**transactionDownload**](docs/Api/TransactionApi.md#transactiondownload)                                           | **GET** /transaction/export                      | Export Transactions                                 |
| _TransactionApi_             | [**transactionEvent**](docs/Api/TransactionApi.md#transactionevent)                                                 | **GET** /transaction/{id}/event                  | Get Transaction Event                               |
| _TransactionApi_             | [**transactionFetch**](docs/Api/TransactionApi.md#transactionfetch)                                                 | **GET** /transaction/{id}                        | Fetch Transaction                                   |
| _TransactionApi_             | [**transactionInitialize**](docs/Api/TransactionApi.md#transactioninitialize)                                       | **POST** /transaction/initialize                 | Initialize Transaction                              |
| _TransactionApi_             | [**transactionList**](docs/Api/TransactionApi.md#transactionlist)                                                   | **GET** /transaction                             | List Transactions                                   |
| _TransactionApi_             | [**transactionPartialDebit**](docs/Api/TransactionApi.md#transactionpartialdebit)                                   | **POST** /transaction/partial_debit              | Partial Debit                                       |
| _TransactionApi_             | [**transactionSession**](docs/Api/TransactionApi.md#transactionsession)                                             | **GET** /transaction/{id}/session                | Get Transaction Session                             |
| _TransactionApi_             | [**transactionTimeline**](docs/Api/TransactionApi.md#transactiontimeline)                                           | **GET** /transaction/timeline/{id}               | Fetch Transaction Timeline                          |
| _TransactionApi_             | [**transactionTotals**](docs/Api/TransactionApi.md#transactiontotals)                                               | **GET** /transaction/totals                      | Transaction Totals                                  |
| _TransactionApi_             | [**transactionVerify**](docs/Api/TransactionApi.md#transactionverify)                                               | **GET** /transaction/verify/{reference}          | Verify Transaction                                  |
| _TransferApi_                | [**transferBulk**](docs/Api/TransferApi.md#transferbulk)                                                            | **POST** /transfer/bulk                          | Initiate Bulk Transfer                              |
| _TransferApi_                | [**transferDisableOtp**](docs/Api/TransferApi.md#transferdisableotp)                                                | **POST** /transfer/disable_otp                   | Disable OTP requirement for Transfers               |
| _TransferApi_                | [**transferDisableOtpFinalize**](docs/Api/TransferApi.md#transferdisableotpfinalize)                                | **POST** /transfer/disable_otp_finalize          | Finalize Disabling of OTP requirement for Transfers |
| _TransferApi_                | [**transferDownload**](docs/Api/TransferApi.md#transferdownload)                                                    | **GET** /transfer/export                         | Export Transfers                                    |
| _TransferApi_                | [**transferEnableOtp**](docs/Api/TransferApi.md#transferenableotp)                                                  | **POST** /transfer/enable_otp                    | Enable OTP requirement for Transfers                |
| _TransferApi_                | [**transferFetch**](docs/Api/TransferApi.md#transferfetch)                                                          | **GET** /transfer/{code}                         | Fetch Transfer                                      |
| _TransferApi_                | [**transferFinalize**](docs/Api/TransferApi.md#transferfinalize)                                                    | **POST** /transfer/finalize_transfer             | Finalize Transfer                                   |
| _TransferApi_                | [**transferInitiate**](docs/Api/TransferApi.md#transferinitiate)                                                    | **POST** /transfer                               | Initiate Transfer                                   |
| _TransferApi_                | [**transferList**](docs/Api/TransferApi.md#transferlist)                                                            | **GET** /transfer                                | List Transfers                                      |
| _TransferApi_                | [**transferResendOtp**](docs/Api/TransferApi.md#transferresendotp)                                                  | **POST** /transfer/resend_otp                    | Resend OTP for Transfer                             |
| _TransferApi_                | [**transferVerify**](docs/Api/TransferApi.md#transferverify)                                                        | **GET** /transfer/verify/{reference}             | Verify Transfer                                     |
| _TransferRecipientApi_       | [**transferrecipientBulk**](docs/Api/TransferRecipientApi.md#transferrecipientbulk)                                 | **POST** /transferrecipient/bulk                 | Bulk Create Transfer Recipient                      |
| _TransferRecipientApi_       | [**transferrecipientCreate**](docs/Api/TransferRecipientApi.md#transferrecipientcreate)                             | **POST** /transferrecipient                      | Create Transfer Recipient                           |
| _TransferRecipientApi_       | [**transferrecipientDelete**](docs/Api/TransferRecipientApi.md#transferrecipientdelete)                             | **DELETE** /transferrecipient/{code}             | Delete Transfer Recipient                           |
| _TransferRecipientApi_       | [**transferrecipientFetch**](docs/Api/TransferRecipientApi.md#transferrecipientfetch)                               | **GET** /transferrecipient/{code}                | Fetch Transfer recipient                            |
| _TransferRecipientApi_       | [**transferrecipientList**](docs/Api/TransferRecipientApi.md#transferrecipientlist)                                 | **GET** /transferrecipient                       | List Transfer Recipients                            |
| _TransferRecipientApi_       | [**transferrecipientUpdate**](docs/Api/TransferRecipientApi.md#transferrecipientupdate)                             | **PUT** /transferrecipient/{code}                | Update Transfer recipient                           |

## Models

- [ApplePayCreateOkModel](docs/Model/ApplePayCreateOkModel.md)
- [ApplePayParam](docs/Model/ApplePayParam.md)
- [BalanceCheckResponse](docs/Model/BalanceCheckResponse.md)
- [BalanceCheckResponseArray](docs/Model/BalanceCheckResponseArray.md)
- [BalanceFetchLedgerResponse](docs/Model/BalanceFetchLedgerResponse.md)
- [BalanceFetchLedgerResponseArray](docs/Model/BalanceFetchLedgerResponseArray.md)
- [Bank](docs/Model/Bank.md)
- [BankValidateRequest](docs/Model/BankValidateRequest.md)
- [BulkChargeFetchBulkBatchChargesResponse](docs/Model/BulkChargeFetchBulkBatchChargesResponse.md)
- [BulkChargeFetchBulkBatchChargesResponseArray](docs/Model/BulkChargeFetchBulkBatchChargesResponseArray.md)
- [BulkChargeFetchBulkBatchChargesResponseMeta](docs/Model/BulkChargeFetchBulkBatchChargesResponseMeta.md)
- [BulkChargeFetchResponse](docs/Model/BulkChargeFetchResponse.md)
- [BulkChargeInitiate](docs/Model/BulkChargeInitiate.md)
- [BulkChargeInitiateRequestInner](docs/Model/BulkChargeInitiateRequestInner.md)
- [BulkChargeInitiateResponse](docs/Model/BulkChargeInitiateResponse.md)
- [BulkChargeInitiateResponseData](docs/Model/BulkChargeInitiateResponseData.md)
- [BulkChargeListResponse](docs/Model/BulkChargeListResponse.md)
- [BulkChargeListResponseArray](docs/Model/BulkChargeListResponseArray.md)
- [BulkChargePauseResponse](docs/Model/BulkChargePauseResponse.md)
- [BulkChargeResumeResponse](docs/Model/BulkChargeResumeResponse.md)
- [ChargeCheckPendingResponse](docs/Model/ChargeCheckPendingResponse.md)
- [ChargeCheckPendingResponseData](docs/Model/ChargeCheckPendingResponseData.md)
- [ChargeCheckPendingResponseDataAuthorization](docs/Model/ChargeCheckPendingResponseDataAuthorization.md)
- [ChargeCreate](docs/Model/ChargeCreate.md)
- [ChargeCreateRequest](docs/Model/ChargeCreateRequest.md)
- [ChargeCreateResponse](docs/Model/ChargeCreateResponse.md)
- [ChargeCreateResponseData](docs/Model/ChargeCreateResponseData.md)
- [ChargeSubmitAddress](docs/Model/ChargeSubmitAddress.md)
- [ChargeSubmitBirthday](docs/Model/ChargeSubmitBirthday.md)
- [ChargeSubmitBirthdayResponse](docs/Model/ChargeSubmitBirthdayResponse.md)
- [ChargeSubmitBirthdayResponseData](docs/Model/ChargeSubmitBirthdayResponseData.md)
- [ChargeSubmitOTP](docs/Model/ChargeSubmitOTP.md)
- [ChargeSubmitOtpResponse](docs/Model/ChargeSubmitOtpResponse.md)
- [ChargeSubmitPhone](docs/Model/ChargeSubmitPhone.md)
- [ChargeSubmitPhoneResponse](docs/Model/ChargeSubmitPhoneResponse.md)
- [ChargeSubmitPhoneResponseData](docs/Model/ChargeSubmitPhoneResponseData.md)
- [ChargeSubmitPin](docs/Model/ChargeSubmitPin.md)
- [ChargeSubmitPinResponse](docs/Model/ChargeSubmitPinResponse.md)
- [ChargeSubmitPinResponseData](docs/Model/ChargeSubmitPinResponseData.md)
- [Currency](docs/Model/Currency.md)
- [CustomerCreate](docs/Model/CustomerCreate.md)
- [CustomerCreateResponse](docs/Model/CustomerCreateResponse.md)
- [CustomerCreateResponseData](docs/Model/CustomerCreateResponseData.md)
- [CustomerCreateResponseDataMetadata](docs/Model/CustomerCreateResponseDataMetadata.md)
- [CustomerDeactivateAuthorization](docs/Model/CustomerDeactivateAuthorization.md)
- [CustomerDeactivateAuthorizationResponse](docs/Model/CustomerDeactivateAuthorizationResponse.md)
- [CustomerFetchResponse](docs/Model/CustomerFetchResponse.md)
- [CustomerFetchResponseData](docs/Model/CustomerFetchResponseData.md)
- [CustomerListResponse](docs/Model/CustomerListResponse.md)
- [CustomerListResponseArray](docs/Model/CustomerListResponseArray.md)
- [CustomerListResponseMeta](docs/Model/CustomerListResponseMeta.md)
- [CustomerRiskAction](docs/Model/CustomerRiskAction.md)
- [CustomerUpdate](docs/Model/CustomerUpdate.md)
- [CustomerUpdateResponse](docs/Model/CustomerUpdateResponse.md)
- [CustomerUpdateResponseData](docs/Model/CustomerUpdateResponseData.md)
- [CustomerValidate](docs/Model/CustomerValidate.md)
- [CustomerValidateResponse](docs/Model/CustomerValidateResponse.md)
- [CustomerWhitelistBlacklistResponse](docs/Model/CustomerWhitelistBlacklistResponse.md)
- [CustomerWhitelistBlacklistResponseData](docs/Model/CustomerWhitelistBlacklistResponseData.md)
- [DedicatedNubanCreateResponse](docs/Model/DedicatedNubanCreateResponse.md)
- [DedicatedNubanCreateResponseData](docs/Model/DedicatedNubanCreateResponseData.md)
- [DedicatedNubanCreateResponseDataAssignment](docs/Model/DedicatedNubanCreateResponseDataAssignment.md)
- [DedicatedNubanDeactivateResponse](docs/Model/DedicatedNubanDeactivateResponse.md)
- [DedicatedNubanDeactivateResponseData](docs/Model/DedicatedNubanDeactivateResponseData.md)
- [DedicatedNubanDeactivateResponseDataAssignment](docs/Model/DedicatedNubanDeactivateResponseDataAssignment.md)
- [DedicatedNubanFetchResponse](docs/Model/DedicatedNubanFetchResponse.md)
- [DedicatedNubanFetchResponseData](docs/Model/DedicatedNubanFetchResponseData.md)
- [DedicatedNubanFetchResponseDataBank](docs/Model/DedicatedNubanFetchResponseDataBank.md)
- [DedicatedNubanFetchResponseDataCustomer](docs/Model/DedicatedNubanFetchResponseDataCustomer.md)
- [DedicatedVirtualAccountAssign](docs/Model/DedicatedVirtualAccountAssign.md)
- [DedicatedVirtualAccountCreate](docs/Model/DedicatedVirtualAccountCreate.md)
- [DedicatedVirtualAccountSplit](docs/Model/DedicatedVirtualAccountSplit.md)
- [DisputeAddEvidenceResponse](docs/Model/DisputeAddEvidenceResponse.md)
- [DisputeAddEvidenceResponseData](docs/Model/DisputeAddEvidenceResponseData.md)
- [DisputeEvidence](docs/Model/DisputeEvidence.md)
- [DisputeExportResponse](docs/Model/DisputeExportResponse.md)
- [DisputeFetchResponse](docs/Model/DisputeFetchResponse.md)
- [DisputeFetchResponseData](docs/Model/DisputeFetchResponseData.md)
- [DisputeFetchResponseDataTransaction](docs/Model/DisputeFetchResponseDataTransaction.md)
- [DisputeFetchResponseDataTransactionAuthorization](docs/Model/DisputeFetchResponseDataTransactionAuthorization.md)
- [DisputeFetchResponseDataTransactionCustomer](docs/Model/DisputeFetchResponseDataTransactionCustomer.md)
- [DisputeHistoryArray](docs/Model/DisputeHistoryArray.md)
- [DisputeListResponse](docs/Model/DisputeListResponse.md)
- [DisputeListResponseArray](docs/Model/DisputeListResponseArray.md)
- [DisputeListResponseArrayTransaction](docs/Model/DisputeListResponseArrayTransaction.md)
- [DisputeListTransactionResponse](docs/Model/DisputeListTransactionResponse.md)
- [DisputeListTransactionResponseData](docs/Model/DisputeListTransactionResponseData.md)
- [DisputeListTransactionResponseDataTransaction](docs/Model/DisputeListTransactionResponseDataTransaction.md)
- [DisputeMessagesArray](docs/Model/DisputeMessagesArray.md)
- [DisputeResolve](docs/Model/DisputeResolve.md)
- [DisputeResolveResponse](docs/Model/DisputeResolveResponse.md)
- [DisputeResolveResponseData](docs/Model/DisputeResolveResponseData.md)
- [DisputeResolveResponseDataMessage](docs/Model/DisputeResolveResponseDataMessage.md)
- [DisputeUpdate](docs/Model/DisputeUpdate.md)
- [DisputeUpdateResponse](docs/Model/DisputeUpdateResponse.md)
- [DisputeUploadURLResponse](docs/Model/DisputeUploadURLResponse.md)
- [DisputeUploadURLResponseData](docs/Model/DisputeUploadURLResponseData.md)
- [EFT](docs/Model/EFT.md)
- [Error](docs/Model/Error.md)
- [ErrorMeta](docs/Model/ErrorMeta.md)
- [ErrorRecordsArray](docs/Model/ErrorRecordsArray.md)
- [MetadataCustomFieldsArray](docs/Model/MetadataCustomFieldsArray.md)
- [MiscellaneousListBanksResponse](docs/Model/MiscellaneousListBanksResponse.md)
- [MiscellaneousListBanksResponseArray](docs/Model/MiscellaneousListBanksResponseArray.md)
- [MiscellaneousListCountriesResponse](docs/Model/MiscellaneousListCountriesResponse.md)
- [MiscellaneousListCountriesResponseArray](docs/Model/MiscellaneousListCountriesResponseArray.md)
- [MiscellaneousListCountriesResponseArrayRelationships](docs/Model/MiscellaneousListCountriesResponseArrayRelationships.md)
- [MiscellaneousListCountriesResponseArrayRelationshipsCurrency](docs/Model/MiscellaneousListCountriesResponseArrayRelationshipsCurrency.md)
- [MiscellaneousListCountriesResponseArrayRelationshipsCurrencySupportedCurrencies](docs/Model/MiscellaneousListCountriesResponseArrayRelationshipsCurrencySupportedCurrencies.md)
- [MiscellaneousListCountriesResponseArrayRelationshipsCurrencySupportedCurrenciesNGN](docs/Model/MiscellaneousListCountriesResponseArrayRelationshipsCurrencySupportedCurrenciesNGN.md)
- [MiscellaneousListCountriesResponseArrayRelationshipsCurrencySupportedCurrenciesNGNBank](docs/Model/MiscellaneousListCountriesResponseArrayRelationshipsCurrencySupportedCurrenciesNGNBank.md)
- [MiscellaneousListCountriesResponseArrayRelationshipsCurrencySupportedCurrenciesNGNBankAccountNumberPattern](docs/Model/MiscellaneousListCountriesResponseArrayRelationshipsCurrencySupportedCurrenciesNGNBankAccountNumberPattern.md)
- [MiscellaneousListCountriesResponseArrayRelationshipsCurrencySupportedCurrenciesUSD](docs/Model/MiscellaneousListCountriesResponseArrayRelationshipsCurrencySupportedCurrenciesUSD.md)
- [MiscellaneousListCountriesResponseArrayRelationshipsCurrencySupportedCurrenciesUSDBank](docs/Model/MiscellaneousListCountriesResponseArrayRelationshipsCurrencySupportedCurrenciesUSDBank.md)
- [MiscellaneousListCountriesResponseArrayRelationshipsIntegrationFeature](docs/Model/MiscellaneousListCountriesResponseArrayRelationshipsIntegrationFeature.md)
- [MiscellaneousListCountriesResponseArrayRelationshipsIntegrationType](docs/Model/MiscellaneousListCountriesResponseArrayRelationshipsIntegrationType.md)
- [MiscellaneousListStatesResponse](docs/Model/MiscellaneousListStatesResponse.md)
- [MiscellaneousListStatesResponseArray](docs/Model/MiscellaneousListStatesResponseArray.md)
- [MobileMoney](docs/Model/MobileMoney.md)
- [OrderCreate](docs/Model/OrderCreate.md)
- [OrderCreateResponse](docs/Model/OrderCreateResponse.md)
- [OrderCreateResponseData](docs/Model/OrderCreateResponseData.md)
- [OrderCreateResponseDataShipping](docs/Model/OrderCreateResponseDataShipping.md)
- [OrderCreateResponseDataShippingMethod](docs/Model/OrderCreateResponseDataShippingMethod.md)
- [OrderFetchProductResponse](docs/Model/OrderFetchProductResponse.md)
- [OrderFetchProductResponseArray](docs/Model/OrderFetchProductResponseArray.md)
- [OrderFetchProductResponseMeta](docs/Model/OrderFetchProductResponseMeta.md)
- [OrderFetchResponse](docs/Model/OrderFetchResponse.md)
- [OrderFetchResponseData](docs/Model/OrderFetchResponseData.md)
- [OrderItems](docs/Model/OrderItems.md)
- [OrderItemsArray](docs/Model/OrderItemsArray.md)
- [OrderListResponse](docs/Model/OrderListResponse.md)
- [OrderListResponseArray](docs/Model/OrderListResponseArray.md)
- [OrderListResponseMeta](docs/Model/OrderListResponseMeta.md)
- [OrderShipping](docs/Model/OrderShipping.md)
- [OrderValidateResponse](docs/Model/OrderValidateResponse.md)
- [OrderValidateResponseData](docs/Model/OrderValidateResponseData.md)
- [OrderValidateResponseDataIntegration](docs/Model/OrderValidateResponseDataIntegration.md)
- [PageAddProductsResponse](docs/Model/PageAddProductsResponse.md)
- [PageAddProductsResponseData](docs/Model/PageAddProductsResponseData.md)
- [PageCheckSlugAvailabilityResponse](docs/Model/PageCheckSlugAvailabilityResponse.md)
- [PageCreate](docs/Model/PageCreate.md)
- [PageCreateResponse](docs/Model/PageCreateResponse.md)
- [PageCreateResponseData](docs/Model/PageCreateResponseData.md)
- [PageFetchResponse](docs/Model/PageFetchResponse.md)
- [PageFetchResponseData](docs/Model/PageFetchResponseData.md)
- [PageListResponse](docs/Model/PageListResponse.md)
- [PageListResponseArray](docs/Model/PageListResponseArray.md)
- [PageProduct](docs/Model/PageProduct.md)
- [PageProductsArray](docs/Model/PageProductsArray.md)
- [PageUpdate](docs/Model/PageUpdate.md)
- [PageUpdateResponse](docs/Model/PageUpdateResponse.md)
- [PageUpdateResponseData](docs/Model/PageUpdateResponseData.md)
- [PaymentRequestArchiveResponse](docs/Model/PaymentRequestArchiveResponse.md)
- [PaymentRequestCreate](docs/Model/PaymentRequestCreate.md)
- [PaymentRequestCreateResponse](docs/Model/PaymentRequestCreateResponse.md)
- [PaymentRequestCreateResponseData](docs/Model/PaymentRequestCreateResponseData.md)
- [PaymentRequestFinalizeResponse](docs/Model/PaymentRequestFinalizeResponse.md)
- [PaymentRequestFinalizeResponseData](docs/Model/PaymentRequestFinalizeResponseData.md)
- [PaymentRequestFinalizeResponseDataDiscount](docs/Model/PaymentRequestFinalizeResponseDataDiscount.md)
- [PaymentRequestLineItemsArray](docs/Model/PaymentRequestLineItemsArray.md)
- [PaymentRequestListResponse](docs/Model/PaymentRequestListResponse.md)
- [PaymentRequestListResponseArray](docs/Model/PaymentRequestListResponseArray.md)
- [PaymentRequestListResponseMeta](docs/Model/PaymentRequestListResponseMeta.md)
- [PaymentRequestListResponseMetaPerPage](docs/Model/PaymentRequestListResponseMetaPerPage.md)
- [PaymentRequestNotificationsArray](docs/Model/PaymentRequestNotificationsArray.md)
- [PaymentRequestPendingArray](docs/Model/PaymentRequestPendingArray.md)
- [PaymentRequestSendNotificationResponse](docs/Model/PaymentRequestSendNotificationResponse.md)
- [PaymentRequestSuccessfulArray](docs/Model/PaymentRequestSuccessfulArray.md)
- [PaymentRequestTaxArray](docs/Model/PaymentRequestTaxArray.md)
- [PaymentRequestTotalArray](docs/Model/PaymentRequestTotalArray.md)
- [PaymentRequestTotalResponse](docs/Model/PaymentRequestTotalResponse.md)
- [PaymentRequestTotalResponseData](docs/Model/PaymentRequestTotalResponseData.md)
- [PaymentRequestUpdate](docs/Model/PaymentRequestUpdate.md)
- [PaymentRequestUpdateResponse](docs/Model/PaymentRequestUpdateResponse.md)
- [PaymentRequestUpdateResponseData](docs/Model/PaymentRequestUpdateResponseData.md)
- [PaymentRequestUpdateResponseDataCustomer](docs/Model/PaymentRequestUpdateResponseDataCustomer.md)
- [PaymentRequestVerifyResponse](docs/Model/PaymentRequestVerifyResponse.md)
- [PaymentRequestVerifyResponseData](docs/Model/PaymentRequestVerifyResponseData.md)
- [PaymentRequestVerifyResponseDataIntegration](docs/Model/PaymentRequestVerifyResponseDataIntegration.md)
- [PaymentSession](docs/Model/PaymentSession.md)
- [PlanCreate](docs/Model/PlanCreate.md)
- [PlanCreateResponse](docs/Model/PlanCreateResponse.md)
- [PlanCreateResponseData](docs/Model/PlanCreateResponseData.md)
- [PlanFetchResponse](docs/Model/PlanFetchResponse.md)
- [PlanFetchResponseData](docs/Model/PlanFetchResponseData.md)
- [PlanListResponse](docs/Model/PlanListResponse.md)
- [PlanListResponseArray](docs/Model/PlanListResponseArray.md)
- [PlanUpdate](docs/Model/PlanUpdate.md)
- [PlanUpdateResponse](docs/Model/PlanUpdateResponse.md)
- [ProductCreate](docs/Model/ProductCreate.md)
- [ProductCreateResponse](docs/Model/ProductCreateResponse.md)
- [ProductCreateResponseData](docs/Model/ProductCreateResponseData.md)
- [ProductDeleteResponse](docs/Model/ProductDeleteResponse.md)
- [ProductFetchResponse](docs/Model/ProductFetchResponse.md)
- [ProductFetchResponseData](docs/Model/ProductFetchResponseData.md)
- [ProductListsResponse](docs/Model/ProductListsResponse.md)
- [ProductListsResponseArray](docs/Model/ProductListsResponseArray.md)
- [ProductListsResponseArrayMetadata](docs/Model/ProductListsResponseArrayMetadata.md)
- [ProductListsResponseArrayShippingFields](docs/Model/ProductListsResponseArrayShippingFields.md)
- [ProductListsResponseMeta](docs/Model/ProductListsResponseMeta.md)
- [ProductUpdate](docs/Model/ProductUpdate.md)
- [ProductUpdateResponse](docs/Model/ProductUpdateResponse.md)
- [ProductUpdateResponseData](docs/Model/ProductUpdateResponseData.md)
- [RefundCreate](docs/Model/RefundCreate.md)
- [RefundCreateResponse](docs/Model/RefundCreateResponse.md)
- [RefundCreateResponseData](docs/Model/RefundCreateResponseData.md)
- [RefundCreateResponseDataTransaction](docs/Model/RefundCreateResponseDataTransaction.md)
- [RefundCreateResponseDataTransactionAuthorization](docs/Model/RefundCreateResponseDataTransactionAuthorization.md)
- [RefundCreateResponseDataTransactionCustomer](docs/Model/RefundCreateResponseDataTransactionCustomer.md)
- [RefundCreateResponseDataTransactionSubaccount](docs/Model/RefundCreateResponseDataTransactionSubaccount.md)
- [RefundFetchResponse](docs/Model/RefundFetchResponse.md)
- [RefundFetchResponseData](docs/Model/RefundFetchResponseData.md)
- [RefundFetchResponseDataCustomer](docs/Model/RefundFetchResponseDataCustomer.md)
- [RefundListResponse](docs/Model/RefundListResponse.md)
- [RefundListResponseArray](docs/Model/RefundListResponseArray.md)
- [RefundListResponseMeta](docs/Model/RefundListResponseMeta.md)
- [Response](docs/Model/Response.md)
- [SplitAddUpdateSubaccountResponse](docs/Model/SplitAddUpdateSubaccountResponse.md)
- [SplitCreate](docs/Model/SplitCreate.md)
- [SplitCreateResponse](docs/Model/SplitCreateResponse.md)
- [SplitCreateResponseData](docs/Model/SplitCreateResponseData.md)
- [SplitFetchResponse](docs/Model/SplitFetchResponse.md)
- [SplitListResponse](docs/Model/SplitListResponse.md)
- [SplitListResponseArray](docs/Model/SplitListResponseArray.md)
- [SplitListResponseMeta](docs/Model/SplitListResponseMeta.md)
- [SplitRemoveSubaccountResponse](docs/Model/SplitRemoveSubaccountResponse.md)
- [SplitSubaccounts](docs/Model/SplitSubaccounts.md)
- [SplitSubaccountsArray](docs/Model/SplitSubaccountsArray.md)
- [SplitSubaccountsArraySubaccount](docs/Model/SplitSubaccountsArraySubaccount.md)
- [SplitUpdate](docs/Model/SplitUpdate.md)
- [SplitUpdateResponse](docs/Model/SplitUpdateResponse.md)
- [StorefrontAddProducts](docs/Model/StorefrontAddProducts.md)
- [StorefrontContactsArray](docs/Model/StorefrontContactsArray.md)
- [StorefrontCreate](docs/Model/StorefrontCreate.md)
- [StorefrontCreateResponse](docs/Model/StorefrontCreateResponse.md)
- [StorefrontCreateResponseData](docs/Model/StorefrontCreateResponseData.md)
- [StorefrontDeleteResponse](docs/Model/StorefrontDeleteResponse.md)
- [StorefrontFetchResponse](docs/Model/StorefrontFetchResponse.md)
- [StorefrontFetchResponseMeta](docs/Model/StorefrontFetchResponseMeta.md)
- [StorefrontListResponse](docs/Model/StorefrontListResponse.md)
- [StorefrontListResponseArray](docs/Model/StorefrontListResponseArray.md)
- [StorefrontUpdate](docs/Model/StorefrontUpdate.md)
- [StorefrontUpdateResponse](docs/Model/StorefrontUpdateResponse.md)
- [SubaccountCreate](docs/Model/SubaccountCreate.md)
- [SubaccountCreateResponse](docs/Model/SubaccountCreateResponse.md)
- [SubaccountCreateResponseData](docs/Model/SubaccountCreateResponseData.md)
- [SubaccountFetchResponse](docs/Model/SubaccountFetchResponse.md)
- [SubaccountFetchResponseData](docs/Model/SubaccountFetchResponseData.md)
- [SubaccountListResponse](docs/Model/SubaccountListResponse.md)
- [SubaccountListResponseArray](docs/Model/SubaccountListResponseArray.md)
- [SubaccountUpdate](docs/Model/SubaccountUpdate.md)
- [SubaccountUpdateResponse](docs/Model/SubaccountUpdateResponse.md)
- [SubaccountUpdateResponseData](docs/Model/SubaccountUpdateResponseData.md)
- [SubscriptionCreate](docs/Model/SubscriptionCreate.md)
- [SubscriptionCreateResponse](docs/Model/SubscriptionCreateResponse.md)
- [SubscriptionCreateResponseData](docs/Model/SubscriptionCreateResponseData.md)
- [SubscriptionDisableResponse](docs/Model/SubscriptionDisableResponse.md)
- [SubscriptionFetchResponse](docs/Model/SubscriptionFetchResponse.md)
- [SubscriptionFetchResponseData](docs/Model/SubscriptionFetchResponseData.md)
- [SubscriptionFetchResponseDataPlan](docs/Model/SubscriptionFetchResponseDataPlan.md)
- [SubscriptionListResponse](docs/Model/SubscriptionListResponse.md)
- [SubscriptionListResponseArray](docs/Model/SubscriptionListResponseArray.md)
- [SubscriptionListResponseArrayAuthorization](docs/Model/SubscriptionListResponseArrayAuthorization.md)
- [SubscriptionListResponseArrayCustomer](docs/Model/SubscriptionListResponseArrayCustomer.md)
- [SubscriptionListResponseArrayPlan](docs/Model/SubscriptionListResponseArrayPlan.md)
- [SubscriptionToggle](docs/Model/SubscriptionToggle.md)
- [TerminalActivationToggle](docs/Model/TerminalActivationToggle.md)
- [TerminalCommissionDeviceResponse](docs/Model/TerminalCommissionDeviceResponse.md)
- [TerminalDecommissionDeviceResponse](docs/Model/TerminalDecommissionDeviceResponse.md)
- [TerminalGetResponse](docs/Model/TerminalGetResponse.md)
- [TerminalGetResponseData](docs/Model/TerminalGetResponseData.md)
- [TerminalGetStatusResponse](docs/Model/TerminalGetStatusResponse.md)
- [TerminalGetStatusResponseData](docs/Model/TerminalGetStatusResponseData.md)
- [TerminalListsResponse](docs/Model/TerminalListsResponse.md)
- [TerminalListsResponseArray](docs/Model/TerminalListsResponseArray.md)
- [TerminalListsResponseMeta](docs/Model/TerminalListsResponseMeta.md)
- [TerminalSendEvent](docs/Model/TerminalSendEvent.md)
- [TerminalSendEventData](docs/Model/TerminalSendEventData.md)
- [TerminalUpate](docs/Model/TerminalUpate.md)
- [TerminalUpdateResponse](docs/Model/TerminalUpdateResponse.md)
- [TransactionChargeAuthorization](docs/Model/TransactionChargeAuthorization.md)
- [TransactionChargeResponse](docs/Model/TransactionChargeResponse.md)
- [TransactionChargeResponseData](docs/Model/TransactionChargeResponseData.md)
- [TransactionChargeResponseDataAuthorization](docs/Model/TransactionChargeResponseDataAuthorization.md)
- [TransactionChargeResponseDataCustomer](docs/Model/TransactionChargeResponseDataCustomer.md)
- [TransactionExportResponse](docs/Model/TransactionExportResponse.md)
- [TransactionExportResponseData](docs/Model/TransactionExportResponseData.md)
- [TransactionFetchResponse](docs/Model/TransactionFetchResponse.md)
- [TransactionFetchResponseData](docs/Model/TransactionFetchResponseData.md)
- [TransactionFetchResponseDataAuthorization](docs/Model/TransactionFetchResponseDataAuthorization.md)
- [TransactionFetchResponseDataCustomer](docs/Model/TransactionFetchResponseDataCustomer.md)
- [TransactionFetchResponseDataMetadata](docs/Model/TransactionFetchResponseDataMetadata.md)
- [TransactionFetchResponseDataSource](docs/Model/TransactionFetchResponseDataSource.md)
- [TransactionInitialize](docs/Model/TransactionInitialize.md)
- [TransactionInitializeBadRequestModel](docs/Model/TransactionInitializeBadRequestModel.md)
- [TransactionInitializeResponse](docs/Model/TransactionInitializeResponse.md)
- [TransactionInitializeResponseData](docs/Model/TransactionInitializeResponseData.md)
- [TransactionListResponse](docs/Model/TransactionListResponse.md)
- [TransactionListResponseArray](docs/Model/TransactionListResponseArray.md)
- [TransactionListResponseArrayAuthorization](docs/Model/TransactionListResponseArrayAuthorization.md)
- [TransactionListResponseArrayCustomer](docs/Model/TransactionListResponseArrayCustomer.md)
- [TransactionListResponseArraySource](docs/Model/TransactionListResponseArraySource.md)
- [TransactionListResponseMeta](docs/Model/TransactionListResponseMeta.md)
- [TransactionListResponseMetaPerPage](docs/Model/TransactionListResponseMetaPerPage.md)
- [TransactionPartialDebit](docs/Model/TransactionPartialDebit.md)
- [TransactionPartialDebitResponse](docs/Model/TransactionPartialDebitResponse.md)
- [TransactionPartialDebitResponseData](docs/Model/TransactionPartialDebitResponseData.md)
- [TransactionPartialDebitResponseDataCustomer](docs/Model/TransactionPartialDebitResponseDataCustomer.md)
- [TransactionPendingTransfersByCurrencyArray](docs/Model/TransactionPendingTransfersByCurrencyArray.md)
- [TransactionTimelineResponse](docs/Model/TransactionTimelineResponse.md)
- [TransactionTotalVolumeByCurrencyArray](docs/Model/TransactionTotalVolumeByCurrencyArray.md)
- [TransactionTotalsResponse](docs/Model/TransactionTotalsResponse.md)
- [TransactionTotalsResponseData](docs/Model/TransactionTotalsResponseData.md)
- [TransactionVerifyResponse](docs/Model/TransactionVerifyResponse.md)
- [TransactionVerifyResponseData](docs/Model/TransactionVerifyResponseData.md)
- [TransactionVerifyResponseDataAuthorization](docs/Model/TransactionVerifyResponseDataAuthorization.md)
- [TransactionVerifyResponseDataCustomer](docs/Model/TransactionVerifyResponseDataCustomer.md)
- [TransactionVerifyResponseDataMetadata](docs/Model/TransactionVerifyResponseDataMetadata.md)
- [TransferBulk](docs/Model/TransferBulk.md)
- [TransferBulkResponse](docs/Model/TransferBulkResponse.md)
- [TransferBulkResponseArray](docs/Model/TransferBulkResponseArray.md)
- [TransferCreateResponse](docs/Model/TransferCreateResponse.md)
- [TransferCreateResponseData](docs/Model/TransferCreateResponseData.md)
- [TransferDisablesOtpResponse](docs/Model/TransferDisablesOtpResponse.md)
- [TransferEnablesOtpResponse](docs/Model/TransferEnablesOtpResponse.md)
- [TransferFeesBreakdownArray](docs/Model/TransferFeesBreakdownArray.md)
- [TransferFetchResponse](docs/Model/TransferFetchResponse.md)
- [TransferFetchResponseData](docs/Model/TransferFetchResponseData.md)
- [TransferFinalize](docs/Model/TransferFinalize.md)
- [TransferFinalizeDisableOTP](docs/Model/TransferFinalizeDisableOTP.md)
- [TransferFinalizeDisablesOtpResponse](docs/Model/TransferFinalizeDisablesOtpResponse.md)
- [TransferInitiate](docs/Model/TransferInitiate.md)
- [TransferListResponse](docs/Model/TransferListResponse.md)
- [TransferListResponseArray](docs/Model/TransferListResponseArray.md)
- [TransferListResponseArrayRecipient](docs/Model/TransferListResponseArrayRecipient.md)
- [TransferListResponseArrayRecipientDetails](docs/Model/TransferListResponseArrayRecipientDetails.md)
- [TransferListResponseArraySession](docs/Model/TransferListResponseArraySession.md)
- [TransferRecipientBulk](docs/Model/TransferRecipientBulk.md)
- [TransferRecipientBulkCreateResponse](docs/Model/TransferRecipientBulkCreateResponse.md)
- [TransferRecipientBulkCreateResponseData](docs/Model/TransferRecipientBulkCreateResponseData.md)
- [TransferRecipientCreate](docs/Model/TransferRecipientCreate.md)
- [TransferRecipientCreateResponse](docs/Model/TransferRecipientCreateResponse.md)
- [TransferRecipientCreateResponseData](docs/Model/TransferRecipientCreateResponseData.md)
- [TransferRecipientDeleteResponse](docs/Model/TransferRecipientDeleteResponse.md)
- [TransferRecipientErrorsArray](docs/Model/TransferRecipientErrorsArray.md)
- [TransferRecipientFetchResponse](docs/Model/TransferRecipientFetchResponse.md)
- [TransferRecipientFetchResponseData](docs/Model/TransferRecipientFetchResponseData.md)
- [TransferRecipientFetchResponseDataDetails](docs/Model/TransferRecipientFetchResponseDataDetails.md)
- [TransferRecipientListResponse](docs/Model/TransferRecipientListResponse.md)
- [TransferRecipientListResponseArray](docs/Model/TransferRecipientListResponseArray.md)
- [TransferRecipientListResponseArrayDetails](docs/Model/TransferRecipientListResponseArrayDetails.md)
- [TransferRecipientUpdate](docs/Model/TransferRecipientUpdate.md)
- [TransferRecipientUpdateResponse](docs/Model/TransferRecipientUpdateResponse.md)
- [TransferResendOTP](docs/Model/TransferResendOTP.md)
- [TransferResendsOtpResponse](docs/Model/TransferResendsOtpResponse.md)
- [TransferVerifyResponse](docs/Model/TransferVerifyResponse.md)
- [TransferVerifyResponseData](docs/Model/TransferVerifyResponseData.md)
- [TransferVerifyResponseDataRecipient](docs/Model/TransferVerifyResponseDataRecipient.md)
- [USSD](docs/Model/USSD.md)
- [VerificationResolveAccountNumberResponse](docs/Model/VerificationResolveAccountNumberResponse.md)
- [VerificationResolveAccountNumberResponseData](docs/Model/VerificationResolveAccountNumberResponseData.md)
- [VerificationResolveCardBINResponse](docs/Model/VerificationResolveCardBINResponse.md)
- [VerificationResolveCardBINResponseData](docs/Model/VerificationResolveCardBINResponseData.md)
- [VerificationValidateAccountResponse](docs/Model/VerificationValidateAccountResponse.md)
- [VerificationValidateAccountResponseData](docs/Model/VerificationValidateAccountResponseData.md)

## Authorization

Authentication schemes defined for the API:

### bearerAuth

- **Type**: Bearer authentication

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author

techsupport@paystack.com

## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `1.0.0`
  - Generator version: `7.13.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
