# Solifyn\DeveloperApi

All URIs are relative to http://localhost:8000, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**developerCreateApiKey()**](DeveloperApi.md#developerCreateApiKey) | **POST** /v1/developer/api-keys | Create Developer API Key |
| [**developerCreateWebhook()**](DeveloperApi.md#developerCreateWebhook) | **POST** /v1/developer/webhooks | Create Webhook Endpoint |
| [**developerDeleteWebhook()**](DeveloperApi.md#developerDeleteWebhook) | **DELETE** /v1/developer/webhooks/{id} | Delete Webhook Endpoint |
| [**developerGetAppPortal()**](DeveloperApi.md#developerGetAppPortal) | **GET** /v1/developer/webhooks/app-portal | Retrieve Hosted Webhooks Portal URL |
| [**developerGetWebhook()**](DeveloperApi.md#developerGetWebhook) | **GET** /v1/developer/webhooks/{id} | Retrieve Webhook Endpoint Details |
| [**developerListApiKeys()**](DeveloperApi.md#developerListApiKeys) | **GET** /v1/developer/api-keys | List Developer API Keys |
| [**developerListWebhookDeliveries()**](DeveloperApi.md#developerListWebhookDeliveries) | **GET** /v1/developer/webhooks/{id}/deliveries | Retrieve Webhook Delivery Logs |
| [**developerListWebhooks()**](DeveloperApi.md#developerListWebhooks) | **GET** /v1/developer/webhooks | List Webhook Endpoints |
| [**developerRevokeApiKey()**](DeveloperApi.md#developerRevokeApiKey) | **DELETE** /v1/developer/api-keys/{id} | Revoke API Key |
| [**developerUpdateWebhook()**](DeveloperApi.md#developerUpdateWebhook) | **PATCH** /v1/developer/webhooks/{id} | Update Webhook Endpoint |


## `developerCreateApiKey()`

```php
developerCreateApiKey($create_api_key_dto): \Solifyn\Model\ApiKeyResponseDto
```

Create Developer API Key

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\DeveloperApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$create_api_key_dto = new \Solifyn\Model\CreateApiKeyDto(); // \Solifyn\Model\CreateApiKeyDto

try {
    $result = $apiInstance->developerCreateApiKey($create_api_key_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeveloperApi->developerCreateApiKey: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_api_key_dto** | [**\Solifyn\Model\CreateApiKeyDto**](../Model/CreateApiKeyDto.md)|  | |

### Return type

[**\Solifyn\Model\ApiKeyResponseDto**](../Model/ApiKeyResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `developerCreateWebhook()`

```php
developerCreateWebhook($create_webhook_endpoint_dto): \Solifyn\Model\WebhookEndpointResponseDto
```

Create Webhook Endpoint

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\DeveloperApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$create_webhook_endpoint_dto = new \Solifyn\Model\CreateWebhookEndpointDto(); // \Solifyn\Model\CreateWebhookEndpointDto

try {
    $result = $apiInstance->developerCreateWebhook($create_webhook_endpoint_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeveloperApi->developerCreateWebhook: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_webhook_endpoint_dto** | [**\Solifyn\Model\CreateWebhookEndpointDto**](../Model/CreateWebhookEndpointDto.md)|  | |

### Return type

[**\Solifyn\Model\WebhookEndpointResponseDto**](../Model/WebhookEndpointResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `developerDeleteWebhook()`

```php
developerDeleteWebhook($id)
```

Delete Webhook Endpoint

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\DeveloperApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | The webhook endpoint ID

try {
    $apiInstance->developerDeleteWebhook($id);
} catch (Exception $e) {
    echo 'Exception when calling DeveloperApi->developerDeleteWebhook: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The webhook endpoint ID | |

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

## `developerGetAppPortal()`

```php
developerGetAppPortal(): \Solifyn\Model\AppPortalUrlResponseDto
```

Retrieve Hosted Webhooks Portal URL

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\DeveloperApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->developerGetAppPortal();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeveloperApi->developerGetAppPortal: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Solifyn\Model\AppPortalUrlResponseDto**](../Model/AppPortalUrlResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `developerGetWebhook()`

```php
developerGetWebhook($id): \Solifyn\Model\WebhookEndpointResponseDto
```

Retrieve Webhook Endpoint Details

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\DeveloperApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | The webhook endpoint ID

try {
    $result = $apiInstance->developerGetWebhook($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeveloperApi->developerGetWebhook: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The webhook endpoint ID | |

### Return type

[**\Solifyn\Model\WebhookEndpointResponseDto**](../Model/WebhookEndpointResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `developerListApiKeys()`

```php
developerListApiKeys(): \Solifyn\Model\ApiKeyResponseDto[]
```

List Developer API Keys

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\DeveloperApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->developerListApiKeys();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeveloperApi->developerListApiKeys: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Solifyn\Model\ApiKeyResponseDto[]**](../Model/ApiKeyResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `developerListWebhookDeliveries()`

```php
developerListWebhookDeliveries($id): \Solifyn\Model\WebhookDeliveryResponseDto[]
```

Retrieve Webhook Delivery Logs

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\DeveloperApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | The webhook endpoint ID

try {
    $result = $apiInstance->developerListWebhookDeliveries($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeveloperApi->developerListWebhookDeliveries: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The webhook endpoint ID | |

### Return type

[**\Solifyn\Model\WebhookDeliveryResponseDto[]**](../Model/WebhookDeliveryResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `developerListWebhooks()`

```php
developerListWebhooks(): \Solifyn\Model\WebhookEndpointResponseDto[]
```

List Webhook Endpoints

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\DeveloperApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->developerListWebhooks();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeveloperApi->developerListWebhooks: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Solifyn\Model\WebhookEndpointResponseDto[]**](../Model/WebhookEndpointResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `developerRevokeApiKey()`

```php
developerRevokeApiKey($id)
```

Revoke API Key

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\DeveloperApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | The API key ID

try {
    $apiInstance->developerRevokeApiKey($id);
} catch (Exception $e) {
    echo 'Exception when calling DeveloperApi->developerRevokeApiKey: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The API key ID | |

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

## `developerUpdateWebhook()`

```php
developerUpdateWebhook($id, $update_webhook_endpoint_dto): \Solifyn\Model\WebhookEndpointResponseDto
```

Update Webhook Endpoint

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\DeveloperApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | The webhook endpoint ID
$update_webhook_endpoint_dto = new \Solifyn\Model\UpdateWebhookEndpointDto(); // \Solifyn\Model\UpdateWebhookEndpointDto

try {
    $result = $apiInstance->developerUpdateWebhook($id, $update_webhook_endpoint_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeveloperApi->developerUpdateWebhook: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The webhook endpoint ID | |
| **update_webhook_endpoint_dto** | [**\Solifyn\Model\UpdateWebhookEndpointDto**](../Model/UpdateWebhookEndpointDto.md)|  | |

### Return type

[**\Solifyn\Model\WebhookEndpointResponseDto**](../Model/WebhookEndpointResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
