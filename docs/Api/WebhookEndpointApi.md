# Solifyn\WebhookEndpointApi

All URIs are relative to https://api.solifyn.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**operationalWebhookControllerCreate()**](WebhookEndpointApi.md#operationalWebhookControllerCreate) | **POST** /v1/operational-webhook/endpoint | Create Operational Webhook Endpoint |
| [**operationalWebhookControllerDelete()**](WebhookEndpointApi.md#operationalWebhookControllerDelete) | **DELETE** /v1/operational-webhook/endpoint/{id} | Delete Operational Webhook Endpoint |
| [**operationalWebhookControllerGet()**](WebhookEndpointApi.md#operationalWebhookControllerGet) | **GET** /v1/operational-webhook/endpoint/{id} | Get Operational Webhook Endpoint |
| [**operationalWebhookControllerGetHeaders()**](WebhookEndpointApi.md#operationalWebhookControllerGetHeaders) | **GET** /v1/operational-webhook/endpoint/{id}/headers | Get Operational Webhook Endpoint Headers |
| [**operationalWebhookControllerGetSecret()**](WebhookEndpointApi.md#operationalWebhookControllerGetSecret) | **GET** /v1/operational-webhook/endpoint/{id}/secret | Get Operational Webhook Endpoint Secret |
| [**operationalWebhookControllerList()**](WebhookEndpointApi.md#operationalWebhookControllerList) | **GET** /v1/operational-webhook/endpoint | List Operational Webhook Endpoints |
| [**operationalWebhookControllerRotateSecret()**](WebhookEndpointApi.md#operationalWebhookControllerRotateSecret) | **POST** /v1/operational-webhook/endpoint/{id}/secret/rotate | Rotate Operational Webhook Endpoint Secret |
| [**operationalWebhookControllerUpdate()**](WebhookEndpointApi.md#operationalWebhookControllerUpdate) | **PUT** /v1/operational-webhook/endpoint/{id} | Update Operational Webhook Endpoint |
| [**operationalWebhookControllerUpdateHeaders()**](WebhookEndpointApi.md#operationalWebhookControllerUpdateHeaders) | **PUT** /v1/operational-webhook/endpoint/{id}/headers | Set Operational Webhook Endpoint Headers |


## `operationalWebhookControllerCreate()`

```php
operationalWebhookControllerCreate($operational_webhook_endpoint_in_dto): \Solifyn\Model\OperationalWebhookEndpointResponseDto
```

Create Operational Webhook Endpoint

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\WebhookEndpointApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$operational_webhook_endpoint_in_dto = new \Solifyn\Model\OperationalWebhookEndpointInDto(); // \Solifyn\Model\OperationalWebhookEndpointInDto

try {
    $result = $apiInstance->operationalWebhookControllerCreate($operational_webhook_endpoint_in_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookEndpointApi->operationalWebhookControllerCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **operational_webhook_endpoint_in_dto** | [**\Solifyn\Model\OperationalWebhookEndpointInDto**](../Model/OperationalWebhookEndpointInDto.md)|  | |

### Return type

[**\Solifyn\Model\OperationalWebhookEndpointResponseDto**](../Model/OperationalWebhookEndpointResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `operationalWebhookControllerDelete()`

```php
operationalWebhookControllerDelete($id)
```

Delete Operational Webhook Endpoint

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\WebhookEndpointApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The endpoint ID or UID

try {
    $apiInstance->operationalWebhookControllerDelete($id);
} catch (Exception $e) {
    echo 'Exception when calling WebhookEndpointApi->operationalWebhookControllerDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The endpoint ID or UID | |

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `operationalWebhookControllerGet()`

```php
operationalWebhookControllerGet($id): \Solifyn\Model\OperationalWebhookEndpointResponseDto
```

Get Operational Webhook Endpoint

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\WebhookEndpointApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The endpoint ID or UID

try {
    $result = $apiInstance->operationalWebhookControllerGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookEndpointApi->operationalWebhookControllerGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The endpoint ID or UID | |

### Return type

[**\Solifyn\Model\OperationalWebhookEndpointResponseDto**](../Model/OperationalWebhookEndpointResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `operationalWebhookControllerGetHeaders()`

```php
operationalWebhookControllerGetHeaders($id): \Solifyn\Model\OperationalWebhookEndpointHeadersResponseDto
```

Get Operational Webhook Endpoint Headers

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\WebhookEndpointApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The endpoint ID or UID

try {
    $result = $apiInstance->operationalWebhookControllerGetHeaders($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookEndpointApi->operationalWebhookControllerGetHeaders: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The endpoint ID or UID | |

### Return type

[**\Solifyn\Model\OperationalWebhookEndpointHeadersResponseDto**](../Model/OperationalWebhookEndpointHeadersResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `operationalWebhookControllerGetSecret()`

```php
operationalWebhookControllerGetSecret($id): \Solifyn\Model\OperationalWebhookEndpointSecretResponseDto
```

Get Operational Webhook Endpoint Secret

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\WebhookEndpointApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The endpoint ID or UID

try {
    $result = $apiInstance->operationalWebhookControllerGetSecret($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookEndpointApi->operationalWebhookControllerGetSecret: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The endpoint ID or UID | |

### Return type

[**\Solifyn\Model\OperationalWebhookEndpointSecretResponseDto**](../Model/OperationalWebhookEndpointSecretResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `operationalWebhookControllerList()`

```php
operationalWebhookControllerList(): \Solifyn\Model\OperationalWebhookEndpointListResponseDto
```

List Operational Webhook Endpoints

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\WebhookEndpointApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->operationalWebhookControllerList();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookEndpointApi->operationalWebhookControllerList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Solifyn\Model\OperationalWebhookEndpointListResponseDto**](../Model/OperationalWebhookEndpointListResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `operationalWebhookControllerRotateSecret()`

```php
operationalWebhookControllerRotateSecret($id, $operational_webhook_endpoint_secret_in_dto)
```

Rotate Operational Webhook Endpoint Secret

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\WebhookEndpointApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The endpoint ID or UID
$operational_webhook_endpoint_secret_in_dto = new \Solifyn\Model\OperationalWebhookEndpointSecretInDto(); // \Solifyn\Model\OperationalWebhookEndpointSecretInDto

try {
    $apiInstance->operationalWebhookControllerRotateSecret($id, $operational_webhook_endpoint_secret_in_dto);
} catch (Exception $e) {
    echo 'Exception when calling WebhookEndpointApi->operationalWebhookControllerRotateSecret: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The endpoint ID or UID | |
| **operational_webhook_endpoint_secret_in_dto** | [**\Solifyn\Model\OperationalWebhookEndpointSecretInDto**](../Model/OperationalWebhookEndpointSecretInDto.md)|  | |

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

## `operationalWebhookControllerUpdate()`

```php
operationalWebhookControllerUpdate($id, $operational_webhook_endpoint_update_dto): \Solifyn\Model\OperationalWebhookEndpointResponseDto
```

Update Operational Webhook Endpoint

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\WebhookEndpointApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The endpoint ID or UID
$operational_webhook_endpoint_update_dto = new \Solifyn\Model\OperationalWebhookEndpointUpdateDto(); // \Solifyn\Model\OperationalWebhookEndpointUpdateDto

try {
    $result = $apiInstance->operationalWebhookControllerUpdate($id, $operational_webhook_endpoint_update_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookEndpointApi->operationalWebhookControllerUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The endpoint ID or UID | |
| **operational_webhook_endpoint_update_dto** | [**\Solifyn\Model\OperationalWebhookEndpointUpdateDto**](../Model/OperationalWebhookEndpointUpdateDto.md)|  | |

### Return type

[**\Solifyn\Model\OperationalWebhookEndpointResponseDto**](../Model/OperationalWebhookEndpointResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `operationalWebhookControllerUpdateHeaders()`

```php
operationalWebhookControllerUpdateHeaders($id, $operational_webhook_endpoint_headers_in_dto)
```

Set Operational Webhook Endpoint Headers

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\WebhookEndpointApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The endpoint ID or UID
$operational_webhook_endpoint_headers_in_dto = new \Solifyn\Model\OperationalWebhookEndpointHeadersInDto(); // \Solifyn\Model\OperationalWebhookEndpointHeadersInDto

try {
    $apiInstance->operationalWebhookControllerUpdateHeaders($id, $operational_webhook_endpoint_headers_in_dto);
} catch (Exception $e) {
    echo 'Exception when calling WebhookEndpointApi->operationalWebhookControllerUpdateHeaders: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The endpoint ID or UID | |
| **operational_webhook_endpoint_headers_in_dto** | [**\Solifyn\Model\OperationalWebhookEndpointHeadersInDto**](../Model/OperationalWebhookEndpointHeadersInDto.md)|  | |

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
