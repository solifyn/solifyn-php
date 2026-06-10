# Solifyn\DiscountsApi

All URIs are relative to https://api.solifyn.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**discountsCreate()**](DiscountsApi.md#discountsCreate) | **POST** /v1/discounts | Create Discount |
| [**discountsDelete()**](DiscountsApi.md#discountsDelete) | **DELETE** /v1/discounts/{id} | Delete Discount |
| [**discountsGet()**](DiscountsApi.md#discountsGet) | **GET** /v1/discounts/{id} | Retrieve Discount |
| [**discountsList()**](DiscountsApi.md#discountsList) | **GET** /v1/discounts | List Discounts |
| [**discountsUpdate()**](DiscountsApi.md#discountsUpdate) | **PATCH** /v1/discounts/{id} | Update Discount |
| [**discountsValidate()**](DiscountsApi.md#discountsValidate) | **GET** /v1/discounts/validate | Validate Code |


## `discountsCreate()`

```php
discountsCreate($discount_create): \Solifyn\Model\Discount
```

Create Discount

Create a new discount code within your active business.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\DiscountsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$discount_create = new \Solifyn\Model\DiscountCreate(); // \Solifyn\Model\DiscountCreate

try {
    $result = $apiInstance->discountsCreate($discount_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DiscountsApi->discountsCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **discount_create** | [**\Solifyn\Model\DiscountCreate**](../Model/DiscountCreate.md)|  | |

### Return type

[**\Solifyn\Model\Discount**](../Model/Discount.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `discountsDelete()`

```php
discountsDelete($id): \Solifyn\Model\LicensesDeactivate200Response
```

Delete Discount

Delete a specific discount code by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\DiscountsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = disc_123; // string | The unique discount ID.

try {
    $result = $apiInstance->discountsDelete($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DiscountsApi->discountsDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The unique discount ID. | |

### Return type

[**\Solifyn\Model\LicensesDeactivate200Response**](../Model/LicensesDeactivate200Response.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `discountsGet()`

```php
discountsGet($id): \Solifyn\Model\Discount
```

Retrieve Discount

Retrieve details of a specific discount code using its ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\DiscountsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = disc_123; // string | The unique discount ID.

try {
    $result = $apiInstance->discountsGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DiscountsApi->discountsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The unique discount ID. | |

### Return type

[**\Solifyn\Model\Discount**](../Model/Discount.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `discountsList()`

```php
discountsList($sorting, $limit, $page, $query, $id): \Solifyn\Model\DiscountsList200Response
```

List Discounts

List and query discounts belonging to your active business with support for fuzzy search by code, pagination, and sorting.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\DiscountsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sorting = 'sorting_example'; // string | Sorting criterion. Add a minus sign - before the criteria name to sort by descending order.
$limit = 10; // float | Size of a page, defaults to 10. Maximum is 100.
$page = 1; // float | Page number, defaults to 1.
$query = 'query_example'; // string | Filter by discount code (fuzzy, case-insensitive).
$id = 'id_example'; // string | Filter by discount ID.

try {
    $result = $apiInstance->discountsList($sorting, $limit, $page, $query, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DiscountsApi->discountsList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sorting** | **string**| Sorting criterion. Add a minus sign - before the criteria name to sort by descending order. | [optional] |
| **limit** | **float**| Size of a page, defaults to 10. Maximum is 100. | [optional] [default to 10] |
| **page** | **float**| Page number, defaults to 1. | [optional] [default to 1] |
| **query** | **string**| Filter by discount code (fuzzy, case-insensitive). | [optional] |
| **id** | **string**| Filter by discount ID. | [optional] |

### Return type

[**\Solifyn\Model\DiscountsList200Response**](../Model/DiscountsList200Response.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `discountsUpdate()`

```php
discountsUpdate($id, $discount_update): \Solifyn\Model\Discount
```

Update Discount

Update details of an existing discount code.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\DiscountsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = disc_123; // string | The unique discount ID.
$discount_update = new \Solifyn\Model\DiscountUpdate(); // \Solifyn\Model\DiscountUpdate

try {
    $result = $apiInstance->discountsUpdate($id, $discount_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DiscountsApi->discountsUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The unique discount ID. | |
| **discount_update** | [**\Solifyn\Model\DiscountUpdate**](../Model/DiscountUpdate.md)|  | |

### Return type

[**\Solifyn\Model\Discount**](../Model/Discount.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `discountsValidate()`

```php
discountsValidate($code, $business_id): \Solifyn\Model\Discount
```

Validate Code

Validate if a specific discount code is active and valid for purchase checkout.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\DiscountsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$code = SAVE20; // string | The plain discount code string
$business_id = biz_123; // string | The business database ID context

try {
    $result = $apiInstance->discountsValidate($code, $business_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DiscountsApi->discountsValidate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**| The plain discount code string | |
| **business_id** | **string**| The business database ID context | |

### Return type

[**\Solifyn\Model\Discount**](../Model/Discount.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
