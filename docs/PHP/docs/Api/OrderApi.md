# OpenAPI\Client\OrderApi

All URIs are relative to *https://paella.test10.ozean12.com/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**merchantPayment**](OrderApi.md#merchantPayment) | **POST** /order/{order_id}/confirm-payment | Merchant payment confirmation
[**orderFullCancellation**](OrderApi.md#orderFullCancellation) | **POST** /order/{order_id}/cancel | Order full cancellation
[**orderPost**](OrderApi.md#orderPost) | **POST** /order | Create new order
[**orderShip**](OrderApi.md#orderShip) | **POST** /order/{order_id}/ship | Create new order
[**patchOrder**](OrderApi.md#patchOrder) | **PATCH** /order/{order_id} | Update order amount / duration
[**retrieveOrder**](OrderApi.md#retrieveOrder) | **GET** /order/{order_id} | Create new order


# **merchantPayment**
> merchantPayment($order_id, $merchant_payment_request)

Merchant payment confirmation

Can be full or partial payment. If was paid too much, only order's amount will be direct debited.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');

$apiInstance = new OpenAPI\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order_id = 'order_id_example'; // string | Order id
$merchant_payment_request = new \OpenAPI\Client\Model\MerchantPaymentRequest(); // \OpenAPI\Client\Model\MerchantPaymentRequest | 

try {
    $apiInstance->merchantPayment($order_id, $merchant_payment_request);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->merchantPayment: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **order_id** | **string**| Order id |
 **merchant_payment_request** | [**\OpenAPI\Client\Model\MerchantPaymentRequest**](../Model/MerchantPaymentRequest.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **orderFullCancellation**
> orderFullCancellation($order_id)

Order full cancellation

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');

$apiInstance = new OpenAPI\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order_id = 'order_id_example'; // string | Order id

try {
    $apiInstance->orderFullCancellation($order_id);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->orderFullCancellation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **order_id** | **string**| Order id |

### Return type

void (empty response body)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **orderPost**
> \OpenAPI\Client\Model\Order orderPost($create_new_order_api)

Create new order

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');

$apiInstance = new OpenAPI\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_new_order_api = new \OpenAPI\Client\Model\CreateNewOrderApi(); // \OpenAPI\Client\Model\CreateNewOrderApi | 

try {
    $result = $apiInstance->orderPost($create_new_order_api);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->orderPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_new_order_api** | [**\OpenAPI\Client\Model\CreateNewOrderApi**](../Model/CreateNewOrderApi.md)|  | [optional]

### Return type

[**\OpenAPI\Client\Model\Order**](../Model/Order.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **orderShip**
> \OpenAPI\Client\Model\Order orderShip($order_id, $ship_order)

Create new order

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');

$apiInstance = new OpenAPI\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order_id = 'order_id_example'; // string | Order id
$ship_order = new \OpenAPI\Client\Model\ShipOrder(); // \OpenAPI\Client\Model\ShipOrder | 

try {
    $result = $apiInstance->orderShip($order_id, $ship_order);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->orderShip: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **order_id** | **string**| Order id |
 **ship_order** | [**\OpenAPI\Client\Model\ShipOrder**](../Model/ShipOrder.md)|  | [optional]

### Return type

[**\OpenAPI\Client\Model\Order**](../Model/Order.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **patchOrder**
> patchOrder($order_id, $patch_order)

Update order amount / duration

- If invoice_number, invoice_url and amount are present, then order amount gets updated.  - But when only duration then duration gets updated.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');

$apiInstance = new OpenAPI\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order_id = 'order_id_example'; // string | Order id
$patch_order = new \OpenAPI\Client\Model\PatchOrder(); // \OpenAPI\Client\Model\PatchOrder | 

try {
    $apiInstance->patchOrder($order_id, $patch_order);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->patchOrder: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **order_id** | **string**| Order id |
 **patch_order** | [**\OpenAPI\Client\Model\PatchOrder**](../Model/PatchOrder.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **retrieveOrder**
> \OpenAPI\Client\Model\Order retrieveOrder($order_id)

Create new order

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');

$apiInstance = new OpenAPI\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order_id = 'order_id_example'; // string | Order id

try {
    $result = $apiInstance->retrieveOrder($order_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->retrieveOrder: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **order_id** | **string**| Order id |

### Return type

[**\OpenAPI\Client\Model\Order**](../Model/Order.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

