# Solifyn\WebhookApi

All URIs are relative to https://api.solifyn.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**webhookControllerHandleSvixWebhook()**](WebhookApi.md#webhookControllerHandleSvixWebhook) | **POST** /v1/webhook/svix |  |
| [**webhookControllerHandleWebhook()**](WebhookApi.md#webhookControllerHandleWebhook) | **POST** /v1/webhook |  |


## `webhookControllerHandleSvixWebhook()`

```php
webhookControllerHandleSvixWebhook()
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\WebhookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $apiInstance->webhookControllerHandleSvixWebhook();
} catch (Exception $e) {
    echo 'Exception when calling WebhookApi->webhookControllerHandleSvixWebhook: ', $e->getMessage(), PHP_EOL;
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

## `webhookControllerHandleWebhook()`

```php
webhookControllerHandleWebhook($business_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\WebhookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$business_id = 'business_id_example'; // string

try {
    $apiInstance->webhookControllerHandleWebhook($business_id);
} catch (Exception $e) {
    echo 'Exception when calling WebhookApi->webhookControllerHandleWebhook: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **business_id** | **string**|  | |

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
