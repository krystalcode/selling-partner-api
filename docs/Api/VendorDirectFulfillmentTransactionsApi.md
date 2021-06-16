# SellingPartnerApi\VendorDirectFulfillmentTransactionsApi

All URIs are relative to https://sellingpartnerapi-na.amazon.com.

Method | HTTP request | Description
------------- | ------------- | -------------
[**getTransactionStatus()**](VendorDirectFulfillmentTransactionsApi.md#getTransactionStatus) | **GET** /vendor/directFulfillment/transactions/v1/transactions/{transactionId} | 


## `getTransactionStatus()`

```php
getTransactionStatus($transaction_id): \SellingPartnerApi\Model\VendorDirectFulfillmentTransactions\GetTransactionResponse
```



Returns the status of the transaction indicated by the specified transactionId.  **Usage Plans:**  | Plan type | Rate (requests per second) | Burst | | ---- | ---- | ---- | |Default| 10 | 10 | |Selling partner specific| Variable | Variable |  The x-amzn-RateLimit-Limit response header returns the usage plan rate limits that were applied to the requested operation. Rate limits for some selling partners will vary from the default rate and burst shown in the table above. For more information, see \"Usage Plans and Rate Limits\" in the Selling Partner API documentation.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// See README for more information on the ConfigurationOptions object
$configurationOptions = new SellingPartnerApi\ConfigurationOptions(
    "amzn1.application-oa2-client.....",
    "abcd....",
    "Aztr|IwEBI....",
    "AKIA....",
    "ABCD....",
    "us-east-1",
    "https://sellingpartnerapi-na.amazon.com",
);
$config = new SellingPartnerApi\Configuration($configurationOptions);

$apiInstance = new SellingPartnerApi\Api\VendorDirectFulfillmentTransactionsApi($config);
$transaction_id = 'transaction_id_example'; // string | Previously returned in the response to the POST request of a specific transaction.

try {
    $result = $apiInstance->getTransactionStatus($transaction_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VendorDirectFulfillmentTransactionsApi->getTransactionStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transaction_id** | **string**| Previously returned in the response to the POST request of a specific transaction. |

### Return type

[**\SellingPartnerApi\Model\VendorDirectFulfillmentTransactions\GetTransactionResponse**](../Model/VendorDirectFulfillmentTransactions/GetTransactionResponse.md)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Top]](#) [[API list]](../)
[[VendorDirectFulfillmentTransactions Model list]](../Model/VendorDirectFulfillmentTransactions)
[[README]](../../README.md)