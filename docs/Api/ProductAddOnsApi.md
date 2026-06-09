# Solifyn\ProductAddOnsApi

All URIs are relative to https://api.solifyn.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**productsCreateAddon()**](ProductAddOnsApi.md#productsCreateAddon) | **POST** /v1/products/{id}/addons | Create Product Add-on |
| [**productsDeleteAddon()**](ProductAddOnsApi.md#productsDeleteAddon) | **DELETE** /v1/products/{id}/addons/{addonId} | Delete Product Add-on |
| [**productsGetAddon()**](ProductAddOnsApi.md#productsGetAddon) | **GET** /v1/products/{id}/addons/{addonId} | Retrieve Product Add-on |
| [**productsListAddons()**](ProductAddOnsApi.md#productsListAddons) | **GET** /v1/products/{id}/addons | List Product Add-ons |
| [**productsListAllAddons()**](ProductAddOnsApi.md#productsListAllAddons) | **GET** /v1/products/all-addons/list | List All Add-ons |
| [**productsUpdateAddon()**](ProductAddOnsApi.md#productsUpdateAddon) | **PATCH** /v1/products/{id}/addons/{addonId} | Update Product Add-on |


## `productsCreateAddon()`

```php
productsCreateAddon($id, $addon_create): \Solifyn\Model\Addon
```

Create Product Add-on

Attach a new add-on configuration to a product.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\ProductAddOnsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = prod_parent_123; // string | The parent product ID.
$addon_create = new \Solifyn\Model\AddonCreate(); // \Solifyn\Model\AddonCreate

try {
    $result = $apiInstance->productsCreateAddon($id, $addon_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductAddOnsApi->productsCreateAddon: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The parent product ID. | |
| **addon_create** | [**\Solifyn\Model\AddonCreate**](../Model/AddonCreate.md)|  | |

### Return type

[**\Solifyn\Model\Addon**](../Model/Addon.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsDeleteAddon()`

```php
productsDeleteAddon($id, $addon_id): \Solifyn\Model\ProductMessageResponseDto
```

Delete Product Add-on

Remove an add-on configuration from a product.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\ProductAddOnsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = prod_parent_123; // string | The parent product ID.
$addon_id = prod_addon_123; // string | The add-on product ID to remove.

try {
    $result = $apiInstance->productsDeleteAddon($id, $addon_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductAddOnsApi->productsDeleteAddon: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The parent product ID. | |
| **addon_id** | **string**| The add-on product ID to remove. | |

### Return type

[**\Solifyn\Model\ProductMessageResponseDto**](../Model/ProductMessageResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsGetAddon()`

```php
productsGetAddon($id, $addon_id): \Solifyn\Model\Addon
```

Retrieve Product Add-on

Retrieve a specific add-on configuration of a product.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\ProductAddOnsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = prod_parent_123; // string | The parent product ID.
$addon_id = prod_addon_123; // string | The add-on product ID.

try {
    $result = $apiInstance->productsGetAddon($id, $addon_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductAddOnsApi->productsGetAddon: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The parent product ID. | |
| **addon_id** | **string**| The add-on product ID. | |

### Return type

[**\Solifyn\Model\Addon**](../Model/Addon.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsListAddons()`

```php
productsListAddons($id): \Solifyn\Model\Addon[]
```

List Product Add-ons

Retrieve all add-on configurations attached to a product.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\ProductAddOnsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = prod_parent_123; // string | The parent product ID.

try {
    $result = $apiInstance->productsListAddons($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductAddOnsApi->productsListAddons: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The parent product ID. | |

### Return type

[**\Solifyn\Model\Addon[]**](../Model/Addon.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsListAllAddons()`

```php
productsListAllAddons()
```

List All Add-ons

Retrieve all configured add-on configurations for the active business.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\ProductAddOnsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $apiInstance->productsListAllAddons();
} catch (Exception $e) {
    echo 'Exception when calling ProductAddOnsApi->productsListAllAddons: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

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

## `productsUpdateAddon()`

```php
productsUpdateAddon($id, $addon_id, $addon_update): \Solifyn\Model\Addon
```

Update Product Add-on

Update an existing add-on configuration for a product.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\ProductAddOnsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = prod_parent_123; // string | The parent product ID.
$addon_id = prod_addon_123; // string | The add-on product ID.
$addon_update = new \Solifyn\Model\AddonUpdate(); // \Solifyn\Model\AddonUpdate

try {
    $result = $apiInstance->productsUpdateAddon($id, $addon_id, $addon_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductAddOnsApi->productsUpdateAddon: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The parent product ID. | |
| **addon_id** | **string**| The add-on product ID. | |
| **addon_update** | [**\Solifyn\Model\AddonUpdate**](../Model/AddonUpdate.md)|  | |

### Return type

[**\Solifyn\Model\Addon**](../Model/Addon.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
