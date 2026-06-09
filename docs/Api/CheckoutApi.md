# Solifyn\CheckoutApi

All URIs are relative to https://api.solifyn.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**checkoutCreate()**](CheckoutApi.md#checkoutCreate) | **POST** /v1/checkout/create | Create Checkout Session |
| [**checkoutCreateCollection()**](CheckoutApi.md#checkoutCreateCollection) | **POST** /v1/checkout/collection/create | Create Collection Checkout Session |
| [**checkoutCreateSetup()**](CheckoutApi.md#checkoutCreateSetup) | **POST** /v1/checkout/setup-configuration | Create Setup Checkout Configuration |
| [**checkoutGetSession()**](CheckoutApi.md#checkoutGetSession) | **GET** /v1/checkout/session/{id} | Get Checkout Session Details |
| [**checkoutPricePreview()**](CheckoutApi.md#checkoutPricePreview) | **GET** /v1/checkout/price-preview | Get Converted Price Preview |
| [**checkoutSupportedCurrencies()**](CheckoutApi.md#checkoutSupportedCurrencies) | **GET** /v1/checkout/supported-currencies | Get Supported Currencies |


## `checkoutCreate()`

```php
checkoutCreate($create_checkout_dto): \Solifyn\Model\CheckoutResponseDto
```

Create Checkout Session

Create a new payment configuration for a product. Returns redirect URLs pointing to the custom checkout layout.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\CheckoutApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$create_checkout_dto = new \Solifyn\Model\CreateCheckoutDto(); // \Solifyn\Model\CreateCheckoutDto

try {
    $result = $apiInstance->checkoutCreate($create_checkout_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CheckoutApi->checkoutCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_checkout_dto** | [**\Solifyn\Model\CreateCheckoutDto**](../Model/CreateCheckoutDto.md)|  | |

### Return type

[**\Solifyn\Model\CheckoutResponseDto**](../Model/CheckoutResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `checkoutCreateCollection()`

```php
checkoutCreateCollection($create_collection_checkout_dto): \Solifyn\Model\CheckoutResponseDto
```

Create Collection Checkout Session

Create a new payment configuration for a product bundle/collection.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\CheckoutApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$create_collection_checkout_dto = new \Solifyn\Model\CreateCollectionCheckoutDto(); // \Solifyn\Model\CreateCollectionCheckoutDto

try {
    $result = $apiInstance->checkoutCreateCollection($create_collection_checkout_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CheckoutApi->checkoutCreateCollection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_collection_checkout_dto** | [**\Solifyn\Model\CreateCollectionCheckoutDto**](../Model/CreateCollectionCheckoutDto.md)|  | |

### Return type

[**\Solifyn\Model\CheckoutResponseDto**](../Model/CheckoutResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `checkoutCreateSetup()`

```php
checkoutCreateSetup($create_setup_checkout_dto)
```

Create Setup Checkout Configuration

Create a new checkout session in setup mode for collecting cards without immediate charge.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\CheckoutApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$create_setup_checkout_dto = new \Solifyn\Model\CreateSetupCheckoutDto(); // \Solifyn\Model\CreateSetupCheckoutDto

try {
    $apiInstance->checkoutCreateSetup($create_setup_checkout_dto);
} catch (Exception $e) {
    echo 'Exception when calling CheckoutApi->checkoutCreateSetup: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_setup_checkout_dto** | [**\Solifyn\Model\CreateSetupCheckoutDto**](../Model/CreateSetupCheckoutDto.md)|  | |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `checkoutGetSession()`

```php
checkoutGetSession($id): \Solifyn\Model\CheckoutSessionDetailsDto
```

Get Checkout Session Details

Retrieve checkout details to mount the custom embedded checkout.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\CheckoutApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = ch_XXXXXXXXXXX; // string | Internal database checkout session ID

try {
    $result = $apiInstance->checkoutGetSession($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CheckoutApi->checkoutGetSession: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Internal database checkout session ID | |

### Return type

[**\Solifyn\Model\CheckoutSessionDetailsDto**](../Model/CheckoutSessionDetailsDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `checkoutPricePreview()`

```php
checkoutPricePreview($product_id, $addons, $currency, $discount, $qty, $custom_price): \Solifyn\Model\PricePreviewResponseDto
```

Get Converted Price Preview

Pre-calculate target currencies, applied discounts, and PWYW values before mounting the checkout.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\CheckoutApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$product_id = prod_z2o92kEl6cYYX; // string | Public product ID
$addons = 'addons_example'; // string
$currency = vnd; // string | Target currency code (ISO)
$discount = 10; // string | Percentage discount rate
$qty = 1; // string | Number of product units
$custom_price = 15; // string | Override price for PWYW products

try {
    $result = $apiInstance->checkoutPricePreview($product_id, $addons, $currency, $discount, $qty, $custom_price);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CheckoutApi->checkoutPricePreview: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **product_id** | **string**| Public product ID | |
| **addons** | **string**|  | |
| **currency** | **string**| Target currency code (ISO) | [optional] |
| **discount** | **string**| Percentage discount rate | [optional] |
| **qty** | **string**| Number of product units | [optional] |
| **custom_price** | **string**| Override price for PWYW products | [optional] |

### Return type

[**\Solifyn\Model\PricePreviewResponseDto**](../Model/PricePreviewResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `checkoutSupportedCurrencies()`

```php
checkoutSupportedCurrencies(): \Solifyn\Model\SupportedCurrenciesResponseDto[]
```

Get Supported Currencies

Retrieve all currencies supported for payouts and conversions.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\CheckoutApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->checkoutSupportedCurrencies();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CheckoutApi->checkoutSupportedCurrencies: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Solifyn\Model\SupportedCurrenciesResponseDto[]**](../Model/SupportedCurrenciesResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
