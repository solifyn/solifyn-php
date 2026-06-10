# Solifyn\ProductsApi

All URIs are relative to https://api.solifyn.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**productsArchive()**](ProductsApi.md#productsArchive) | **DELETE** /v1/products/{id} | Archive Product |
| [**productsCreate()**](ProductsApi.md#productsCreate) | **POST** /v1/products | Create Product |
| [**productsGet()**](ProductsApi.md#productsGet) | **GET** /v1/products/{id} | Retrieve Product |
| [**productsList()**](ProductsApi.md#productsList) | **GET** /v1/products | List Products |
| [**productsUnarchive()**](ProductsApi.md#productsUnarchive) | **POST** /v1/products/{id}/unarchive | Unarchive Product |
| [**productsUpdate()**](ProductsApi.md#productsUpdate) | **PATCH** /v1/products/{id} | Update Product |


## `productsArchive()`

```php
productsArchive($id): \Solifyn\Model\ProductsArchive200Response
```

Archive Product

Archive a specific product to hide it from checkout pages and search results. Products are soft-deleted (archived) and can be restored using the unarchive endpoint.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\ProductsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = prod_123; // string | The unique product ID to archive.

try {
    $result = $apiInstance->productsArchive($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->productsArchive: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The unique product ID to archive. | |

### Return type

[**\Solifyn\Model\ProductsArchive200Response**](../Model/ProductsArchive200Response.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsCreate()`

```php
productsCreate($product_create): \Solifyn\Model\Product
```

Create Product

Create a new product within your active business.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\ProductsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$product_create = new \Solifyn\Model\ProductCreate(); // \Solifyn\Model\ProductCreate

try {
    $result = $apiInstance->productsCreate($product_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->productsCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **product_create** | [**\Solifyn\Model\ProductCreate**](../Model/ProductCreate.md)|  | |

### Return type

[**\Solifyn\Model\Product**](../Model/Product.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsGet()`

```php
productsGet($id): \Solifyn\Model\Product
```

Retrieve Product

Retrieve details of a specific product using its ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\ProductsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = prod_123; // string | The unique product ID.

try {
    $result = $apiInstance->productsGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->productsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The unique product ID. | |

### Return type

[**\Solifyn\Model\Product**](../Model/Product.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsList()`

```php
productsList($pricing_type, $sorting, $limit, $page, $is_recurring, $is_archived, $query, $id): \Solifyn\Model\ProductsList200Response
```

List Products

List and query products belonging to your active business with support for fuzzy search, filters, pagination, and sorting.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\ProductsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$pricing_type = 'pricing_type_example'; // string | Filter by pricing type.
$sorting = 'sorting_example'; // string | Sorting criterion. Add a minus sign - before the criteria name to sort by descending order.
$limit = 10; // float | Size of a page, defaults to 10. Maximum is 100.
$page = 1; // float | Page number, defaults to 1.
$is_recurring = True; // bool | Filter on recurring products (subscriptions). If true, only subscription tiers are returned. If false, only one-time purchase products are returned.
$is_archived = True; // bool | Filter by archived status.
$query = 'query_example'; // string | Filter by product name (fuzzy, case-insensitive).
$id = 'id_example'; // string | Filter by product ID.

try {
    $result = $apiInstance->productsList($pricing_type, $sorting, $limit, $page, $is_recurring, $is_archived, $query, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->productsList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **pricing_type** | **string**| Filter by pricing type. | [optional] |
| **sorting** | **string**| Sorting criterion. Add a minus sign - before the criteria name to sort by descending order. | [optional] |
| **limit** | **float**| Size of a page, defaults to 10. Maximum is 100. | [optional] [default to 10] |
| **page** | **float**| Page number, defaults to 1. | [optional] [default to 1] |
| **is_recurring** | **bool**| Filter on recurring products (subscriptions). If true, only subscription tiers are returned. If false, only one-time purchase products are returned. | [optional] |
| **is_archived** | **bool**| Filter by archived status. | [optional] |
| **query** | **string**| Filter by product name (fuzzy, case-insensitive). | [optional] |
| **id** | **string**| Filter by product ID. | [optional] |

### Return type

[**\Solifyn\Model\ProductsList200Response**](../Model/ProductsList200Response.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsUnarchive()`

```php
productsUnarchive($id): \Solifyn\Model\ProductsUnarchive200Response
```

Unarchive Product

Restore an archived product back to active status, making it visible again.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\ProductsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = prod_123; // string | The unique product ID to unarchive.

try {
    $result = $apiInstance->productsUnarchive($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->productsUnarchive: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The unique product ID to unarchive. | |

### Return type

[**\Solifyn\Model\ProductsUnarchive200Response**](../Model/ProductsUnarchive200Response.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsUpdate()`

```php
productsUpdate($id, $product_update): \Solifyn\Model\ProductMessageResponseDto
```

Update Product

Update details of an existing product.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\ProductsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = prod_123; // string | The unique product ID.
$product_update = new \Solifyn\Model\ProductUpdate(); // \Solifyn\Model\ProductUpdate

try {
    $result = $apiInstance->productsUpdate($id, $product_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->productsUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The unique product ID. | |
| **product_update** | [**\Solifyn\Model\ProductUpdate**](../Model/ProductUpdate.md)|  | |

### Return type

[**\Solifyn\Model\ProductMessageResponseDto**](../Model/ProductMessageResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
