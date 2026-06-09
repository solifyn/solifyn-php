# Solifyn\RefundsChargebacksApi

All URIs are relative to https://api.solifyn.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**refundsCreate()**](RefundsChargebacksApi.md#refundsCreate) | **POST** /v1/orders/{id}/refund | Create Refund |
| [**refundsGet()**](RefundsChargebacksApi.md#refundsGet) | **GET** /v1/refunds/{id} | Retrieve Refund details |
| [**refundsList()**](RefundsChargebacksApi.md#refundsList) | **GET** /v1/refunds | List Refunds |


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


$apiInstance = new Solifyn\Api\RefundsChargebacksApi(
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
    echo 'Exception when calling RefundsChargebacksApi->refundsCreate: ', $e->getMessage(), PHP_EOL;
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

## `refundsGet()`

```php
refundsGet($id): \Solifyn\Model\Refund
```

Retrieve Refund details

Get parameters of a specific processed refund by database ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\RefundsChargebacksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = ref_123; // string | Refund ID

try {
    $result = $apiInstance->refundsGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RefundsChargebacksApi->refundsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Refund ID | |

### Return type

[**\Solifyn\Model\Refund**](../Model/Refund.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `refundsList()`

```php
refundsList(): \Solifyn\Model\Refund[]
```

List Refunds

Retrieve a list of processed refunds and chargeback transactions.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\RefundsChargebacksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->refundsList();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RefundsChargebacksApi->refundsList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Solifyn\Model\Refund[]**](../Model/Refund.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
