# Solifyn\CollectionsApi

All URIs are relative to https://api.solifyn.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**collectionsAddProducts()**](CollectionsApi.md#collectionsAddProducts) | **POST** /v1/collections/{id}/products | Add Products to Collection |
| [**collectionsArchive()**](CollectionsApi.md#collectionsArchive) | **DELETE** /v1/collections/{id} | Archive Collection |
| [**collectionsCreate()**](CollectionsApi.md#collectionsCreate) | **POST** /v1/collections | Create Collection |
| [**collectionsDeleteProduct()**](CollectionsApi.md#collectionsDeleteProduct) | **DELETE** /v1/collections/{id}/products/{productId} | Remove Product from Collection |
| [**collectionsGet()**](CollectionsApi.md#collectionsGet) | **GET** /v1/collections/{id} | Retrieve Collection |
| [**collectionsList()**](CollectionsApi.md#collectionsList) | **GET** /v1/collections | List Collections |
| [**collectionsListArchived()**](CollectionsApi.md#collectionsListArchived) | **GET** /v1/collections/archived | List Archived Collections |
| [**collectionsUnarchive()**](CollectionsApi.md#collectionsUnarchive) | **POST** /v1/collections/{id}/unarchive | Unarchive Collection |
| [**collectionsUpdate()**](CollectionsApi.md#collectionsUpdate) | **PATCH** /v1/collections/{id} | Update Collection |
| [**collectionsUpdateProduct()**](CollectionsApi.md#collectionsUpdateProduct) | **PATCH** /v1/collections/{id}/products/{productId} | Update Collection Product |


## `collectionsAddProducts()`

```php
collectionsAddProducts($id, $add_collection_products_dto): \Solifyn\Model\CollectionResponseDto
```

Add Products to Collection

Add one or more products to a collection. If a product already exists, its quantity is updated.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\CollectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = col_123; // string | Collection ID
$add_collection_products_dto = new \Solifyn\Model\AddCollectionProductsDto(); // \Solifyn\Model\AddCollectionProductsDto

try {
    $result = $apiInstance->collectionsAddProducts($id, $add_collection_products_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CollectionsApi->collectionsAddProducts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Collection ID | |
| **add_collection_products_dto** | [**\Solifyn\Model\AddCollectionProductsDto**](../Model/AddCollectionProductsDto.md)|  | |

### Return type

[**\Solifyn\Model\CollectionResponseDto**](../Model/CollectionResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `collectionsArchive()`

```php
collectionsArchive($id): \Solifyn\Model\CollectionArchivedResponseDto
```

Archive Collection

Deactivate and move a collection to archives.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\CollectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = col_123; // string | Collection ID

try {
    $result = $apiInstance->collectionsArchive($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CollectionsApi->collectionsArchive: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Collection ID | |

### Return type

[**\Solifyn\Model\CollectionArchivedResponseDto**](../Model/CollectionArchivedResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `collectionsCreate()`

```php
collectionsCreate($create_collection_dto): \Solifyn\Model\CollectionResponseDto
```

Create Collection

Generate a new product collection for checkout packaging.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\CollectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_collection_dto = new \Solifyn\Model\CreateCollectionDto(); // \Solifyn\Model\CreateCollectionDto

try {
    $result = $apiInstance->collectionsCreate($create_collection_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CollectionsApi->collectionsCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_collection_dto** | [**\Solifyn\Model\CreateCollectionDto**](../Model/CreateCollectionDto.md)|  | |

### Return type

[**\Solifyn\Model\CollectionResponseDto**](../Model/CollectionResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `collectionsDeleteProduct()`

```php
collectionsDeleteProduct($id, $product_id): \Solifyn\Model\CollectionProductDeletedResponseDto
```

Remove Product from Collection

Remove a product from a collection.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\CollectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = col_123; // string | Collection ID
$product_id = prod_123; // string | Product ID

try {
    $result = $apiInstance->collectionsDeleteProduct($id, $product_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CollectionsApi->collectionsDeleteProduct: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Collection ID | |
| **product_id** | **string**| Product ID | |

### Return type

[**\Solifyn\Model\CollectionProductDeletedResponseDto**](../Model/CollectionProductDeletedResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `collectionsGet()`

```php
collectionsGet($id): \Solifyn\Model\CollectionDetailResponseDto
```

Retrieve Collection

Get properties of a product collection by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\CollectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = col_123; // string | Collection ID

try {
    $result = $apiInstance->collectionsGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CollectionsApi->collectionsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Collection ID | |

### Return type

[**\Solifyn\Model\CollectionDetailResponseDto**](../Model/CollectionDetailResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `collectionsList()`

```php
collectionsList(): \Solifyn\Model\CollectionResponseDto[]
```

List Collections

Get all active product collections linked to the current active business.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\CollectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->collectionsList();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CollectionsApi->collectionsList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Solifyn\Model\CollectionResponseDto[]**](../Model/CollectionResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `collectionsListArchived()`

```php
collectionsListArchived(): \Solifyn\Model\CollectionResponseDto[]
```

List Archived Collections

Get all archived/deactivated product collections.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\CollectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->collectionsListArchived();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CollectionsApi->collectionsListArchived: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Solifyn\Model\CollectionResponseDto[]**](../Model/CollectionResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `collectionsUnarchive()`

```php
collectionsUnarchive($id): \Solifyn\Model\CollectionUnarchivedResponseDto
```

Unarchive Collection

Restore an archived collection back to active status.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\CollectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = col_123; // string | Collection ID

try {
    $result = $apiInstance->collectionsUnarchive($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CollectionsApi->collectionsUnarchive: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Collection ID | |

### Return type

[**\Solifyn\Model\CollectionUnarchivedResponseDto**](../Model/CollectionUnarchivedResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `collectionsUpdate()`

```php
collectionsUpdate($id, $update_collection_dto): \Solifyn\Model\CollectionUpdatedResponseDto
```

Update Collection

Update products, friendly name, status, or description of a collection.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\CollectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = col_123; // string | Collection ID
$update_collection_dto = new \Solifyn\Model\UpdateCollectionDto(); // \Solifyn\Model\UpdateCollectionDto

try {
    $result = $apiInstance->collectionsUpdate($id, $update_collection_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CollectionsApi->collectionsUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Collection ID | |
| **update_collection_dto** | [**\Solifyn\Model\UpdateCollectionDto**](../Model/UpdateCollectionDto.md)|  | |

### Return type

[**\Solifyn\Model\CollectionUpdatedResponseDto**](../Model/CollectionUpdatedResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `collectionsUpdateProduct()`

```php
collectionsUpdateProduct($id, $product_id, $update_collection_product_dto): \Solifyn\Model\CollectionProductUpdatedResponseDto
```

Update Collection Product

Update quantity of a specific product inside a collection.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\CollectionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = col_123; // string | Collection ID
$product_id = prod_123; // string | Product ID
$update_collection_product_dto = new \Solifyn\Model\UpdateCollectionProductDto(); // \Solifyn\Model\UpdateCollectionProductDto

try {
    $result = $apiInstance->collectionsUpdateProduct($id, $product_id, $update_collection_product_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CollectionsApi->collectionsUpdateProduct: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Collection ID | |
| **product_id** | **string**| Product ID | |
| **update_collection_product_dto** | [**\Solifyn\Model\UpdateCollectionProductDto**](../Model/UpdateCollectionProductDto.md)|  | |

### Return type

[**\Solifyn\Model\CollectionProductUpdatedResponseDto**](../Model/CollectionProductUpdatedResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
