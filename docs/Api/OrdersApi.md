# Solifyn\OrdersApi

All URIs are relative to https://api.solifyn.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**ordersGet()**](OrdersApi.md#ordersGet) | **GET** /v1/orders/{id} | Retrieve Order |
| [**ordersGetInvoice()**](OrdersApi.md#ordersGetInvoice) | **GET** /v1/orders/{id}/invoice | Get Order Invoice |
| [**ordersList()**](OrdersApi.md#ordersList) | **GET** /v1/orders | List Orders |
| [**ordersUpdate()**](OrdersApi.md#ordersUpdate) | **PATCH** /v1/orders/{id} | Update Order Billing Address |
| [**refundsCreate()**](OrdersApi.md#refundsCreate) | **POST** /v1/orders/{id}/refund | Create Refund |


## `ordersGet()`

```php
ordersGet($id): \Solifyn\Model\Order
```

Retrieve Order

Retrieve details of a specific order/payment by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\OrdersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = pay_123; // string | The unique order/payment ID.

try {
    $result = $apiInstance->ordersGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->ordersGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The unique order/payment ID. | |

### Return type

[**\Solifyn\Model\Order**](../Model/Order.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `ordersGetInvoice()`

```php
ordersGetInvoice($id): \Solifyn\Model\Invoice
```

Get Order Invoice

Retrieve the generated invoice details for the specified order.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\OrdersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = pay_123; // string | The unique order/payment ID.

try {
    $result = $apiInstance->ordersGetInvoice($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->ordersGetInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The unique order/payment ID. | |

### Return type

[**\Solifyn\Model\Invoice**](../Model/Invoice.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `ordersList()`

```php
ordersList($created_at_lte, $created_at_gte, $product_id, $customer_id, $status, $page_size, $page_number): \Solifyn\Model\OrderList
```

List Orders

List and query orders/payments belonging to your active business.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\OrdersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$created_at_lte = 'created_at_lte_example'; // string | Filter by creation date less than or equal to.
$created_at_gte = 'created_at_gte_example'; // string | Filter by creation date greater than or equal to.
$product_id = 'product_id_example'; // string | Filter by product identifier.
$customer_id = 'customer_id_example'; // string | Filter by customer identifier.
$status = 'status_example'; // string | Filter by order/payment status.
$page_size = 10; // float | Size of a page, defaults to 10. Maximum is 100.
$page_number = 1; // float | Page number, defaults to 1.

try {
    $result = $apiInstance->ordersList($created_at_lte, $created_at_gte, $product_id, $customer_id, $status, $page_size, $page_number);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->ordersList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **created_at_lte** | **string**| Filter by creation date less than or equal to. | [optional] |
| **created_at_gte** | **string**| Filter by creation date greater than or equal to. | [optional] |
| **product_id** | **string**| Filter by product identifier. | [optional] |
| **customer_id** | **string**| Filter by customer identifier. | [optional] |
| **status** | **string**| Filter by order/payment status. | [optional] |
| **page_size** | **float**| Size of a page, defaults to 10. Maximum is 100. | [optional] [default to 10] |
| **page_number** | **float**| Page number, defaults to 1. | [optional] [default to 1] |

### Return type

[**\Solifyn\Model\OrderList**](../Model/OrderList.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `ordersUpdate()`

```php
ordersUpdate($id, $order_update): \Solifyn\Model\Order
```

Update Order Billing Address

Update the billing details of an existing order.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\OrdersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = pay_123; // string | The unique order/payment ID.
$order_update = new \Solifyn\Model\OrderUpdate(); // \Solifyn\Model\OrderUpdate

try {
    $result = $apiInstance->ordersUpdate($id, $order_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->ordersUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The unique order/payment ID. | |
| **order_update** | [**\Solifyn\Model\OrderUpdate**](../Model/OrderUpdate.md)|  | |

### Return type

[**\Solifyn\Model\Order**](../Model/Order.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `refundsCreate()`

```php
refundsCreate($id, $order_refund_create)
```

Create Refund

Initiate a full or partial refund for a specific payment/order.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\OrdersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = pay_123; // string | The unique order/payment ID.
$order_refund_create = new \Solifyn\Model\OrderRefundCreate(); // \Solifyn\Model\OrderRefundCreate

try {
    $apiInstance->refundsCreate($id, $order_refund_create);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->refundsCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The unique order/payment ID. | |
| **order_refund_create** | [**\Solifyn\Model\OrderRefundCreate**](../Model/OrderRefundCreate.md)|  | |

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
