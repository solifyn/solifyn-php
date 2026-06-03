# Solifyn\RefundRequestsApi

All URIs are relative to http://localhost:8000, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**refundRequestsList()**](RefundRequestsApi.md#refundRequestsList) | **GET** /v1/refund-requests | List Refund Requests (Merchant) |
| [**refundRequestsListMessages()**](RefundRequestsApi.md#refundRequestsListMessages) | **GET** /v1/refund-requests/{id}/messages | List Messages for Refund Request (Merchant) |
| [**refundRequestsSendMessage()**](RefundRequestsApi.md#refundRequestsSendMessage) | **POST** /v1/refund-requests/{id}/messages | Send Refund Request Message (Merchant) |
| [**refundRequestsUpdateStatus()**](RefundRequestsApi.md#refundRequestsUpdateStatus) | **PATCH** /v1/refund-requests/{id}/status | Update Refund Request Status (Merchant) |
| [**refundRequestsUploadEvidence()**](RefundRequestsApi.md#refundRequestsUploadEvidence) | **POST** /v1/refund-requests/upload-evidence | Upload Dispute Evidence File (Merchant) |


## `refundRequestsList()`

```php
refundRequestsList()
```

List Refund Requests (Merchant)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\RefundRequestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $apiInstance->refundRequestsList();
} catch (Exception $e) {
    echo 'Exception when calling RefundRequestsApi->refundRequestsList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `refundRequestsListMessages()`

```php
refundRequestsListMessages($id)
```

List Messages for Refund Request (Merchant)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\RefundRequestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string

try {
    $apiInstance->refundRequestsListMessages($id);
} catch (Exception $e) {
    echo 'Exception when calling RefundRequestsApi->refundRequestsListMessages: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `refundRequestsSendMessage()`

```php
refundRequestsSendMessage($id)
```

Send Refund Request Message (Merchant)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\RefundRequestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string

try {
    $apiInstance->refundRequestsSendMessage($id);
} catch (Exception $e) {
    echo 'Exception when calling RefundRequestsApi->refundRequestsSendMessage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `refundRequestsUpdateStatus()`

```php
refundRequestsUpdateStatus($id)
```

Update Refund Request Status (Merchant)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\RefundRequestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string

try {
    $apiInstance->refundRequestsUpdateStatus($id);
} catch (Exception $e) {
    echo 'Exception when calling RefundRequestsApi->refundRequestsUpdateStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `refundRequestsUploadEvidence()`

```php
refundRequestsUploadEvidence()
```

Upload Dispute Evidence File (Merchant)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\RefundRequestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $apiInstance->refundRequestsUploadEvidence();
} catch (Exception $e) {
    echo 'Exception when calling RefundRequestsApi->refundRequestsUploadEvidence: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
