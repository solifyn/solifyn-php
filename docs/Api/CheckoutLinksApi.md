# Solifyn\CheckoutLinksApi

All URIs are relative to https://api.solifyn.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**checkoutLinksCreate()**](CheckoutLinksApi.md#checkoutLinksCreate) | **POST** /v1/checkout-links | Create Checkout Link |
| [**checkoutLinksDelete()**](CheckoutLinksApi.md#checkoutLinksDelete) | **DELETE** /v1/checkout-links/{id} | Delete Checkout Link |
| [**checkoutLinksGet()**](CheckoutLinksApi.md#checkoutLinksGet) | **GET** /v1/checkout-links/{id} | Retrieve Checkout Link Details |
| [**checkoutLinksList()**](CheckoutLinksApi.md#checkoutLinksList) | **GET** /v1/checkout-links | List Checkout Links |
| [**checkoutLinksUpdate()**](CheckoutLinksApi.md#checkoutLinksUpdate) | **PATCH** /v1/checkout-links/{id} | Update Checkout Link |


## `checkoutLinksCreate()`

```php
checkoutLinksCreate($create_checkout_link_dto): \Solifyn\Model\CheckoutLinkResponseDto
```

Create Checkout Link

Generate a new checkout session link.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\CheckoutLinksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_checkout_link_dto = new \Solifyn\Model\CreateCheckoutLinkDto(); // \Solifyn\Model\CreateCheckoutLinkDto

try {
    $result = $apiInstance->checkoutLinksCreate($create_checkout_link_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CheckoutLinksApi->checkoutLinksCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_checkout_link_dto** | [**\Solifyn\Model\CreateCheckoutLinkDto**](../Model/CreateCheckoutLinkDto.md)|  | |

### Return type

[**\Solifyn\Model\CheckoutLinkResponseDto**](../Model/CheckoutLinkResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `checkoutLinksDelete()`

```php
checkoutLinksDelete($id): \Solifyn\Model\CheckoutLinkMessageResponseDto
```

Delete Checkout Link

Permanently remove a checkout link.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\CheckoutLinksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = chk_123; // string | Checkout Link ID

try {
    $result = $apiInstance->checkoutLinksDelete($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CheckoutLinksApi->checkoutLinksDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Checkout Link ID | |

### Return type

[**\Solifyn\Model\CheckoutLinkMessageResponseDto**](../Model/CheckoutLinkMessageResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `checkoutLinksGet()`

```php
checkoutLinksGet($id): \Solifyn\Model\CheckoutLinkResponseDto
```

Retrieve Checkout Link Details

Get details of a specific checkout link by ID (public access).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\CheckoutLinksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = chk_123; // string | Checkout Link ID

try {
    $result = $apiInstance->checkoutLinksGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CheckoutLinksApi->checkoutLinksGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Checkout Link ID | |

### Return type

[**\Solifyn\Model\CheckoutLinkResponseDto**](../Model/CheckoutLinkResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `checkoutLinksList()`

```php
checkoutLinksList(): \Solifyn\Model\CheckoutLinkResponseDto[]
```

List Checkout Links

Retrieve all active checkout session links for the active business.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\CheckoutLinksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->checkoutLinksList();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CheckoutLinksApi->checkoutLinksList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Solifyn\Model\CheckoutLinkResponseDto[]**](../Model/CheckoutLinkResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `checkoutLinksUpdate()`

```php
checkoutLinksUpdate($id, $update_checkout_link_dto): \Solifyn\Model\CheckoutLinkMessageResponseDto
```

Update Checkout Link

Update title, custom pricing, redirection URLs, or friendly inputs for a checkout link.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\CheckoutLinksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = chk_123; // string | Checkout Link ID
$update_checkout_link_dto = new \Solifyn\Model\UpdateCheckoutLinkDto(); // \Solifyn\Model\UpdateCheckoutLinkDto

try {
    $result = $apiInstance->checkoutLinksUpdate($id, $update_checkout_link_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CheckoutLinksApi->checkoutLinksUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Checkout Link ID | |
| **update_checkout_link_dto** | [**\Solifyn\Model\UpdateCheckoutLinkDto**](../Model/UpdateCheckoutLinkDto.md)|  | |

### Return type

[**\Solifyn\Model\CheckoutLinkMessageResponseDto**](../Model/CheckoutLinkMessageResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
