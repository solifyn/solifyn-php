# Solifyn\EntitlementsApi

All URIs are relative to https://api.solifyn.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**entitlementsCreate()**](EntitlementsApi.md#entitlementsCreate) | **POST** /v1/entitlements | Create Entitlement |
| [**entitlementsDelete()**](EntitlementsApi.md#entitlementsDelete) | **DELETE** /v1/entitlements/{id} | Delete Entitlement |
| [**entitlementsGet()**](EntitlementsApi.md#entitlementsGet) | **GET** /v1/entitlements/{id} | Retrieve Entitlement |
| [**entitlementsList()**](EntitlementsApi.md#entitlementsList) | **GET** /v1/entitlements | List Entitlements |
| [**entitlementsUpdate()**](EntitlementsApi.md#entitlementsUpdate) | **PATCH** /v1/entitlements/{id} | Update Entitlement |


## `entitlementsCreate()`

```php
entitlementsCreate($create_entitlement_dto): \Solifyn\Model\EntitlementDetailResponseDto
```

Create Entitlement

Create a new independent access entitlement.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\EntitlementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$create_entitlement_dto = new \Solifyn\Model\CreateEntitlementDto(); // \Solifyn\Model\CreateEntitlementDto

try {
    $result = $apiInstance->entitlementsCreate($create_entitlement_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EntitlementsApi->entitlementsCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_entitlement_dto** | [**\Solifyn\Model\CreateEntitlementDto**](../Model/CreateEntitlementDto.md)|  | |

### Return type

[**\Solifyn\Model\EntitlementDetailResponseDto**](../Model/EntitlementDetailResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `entitlementsDelete()`

```php
entitlementsDelete($id): \Solifyn\Model\EntitlementDetailResponseDto
```

Delete Entitlement

Delete an independent entitlement and unlink all mapped products.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\EntitlementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = ent_8Z1aB2cD3eF4gH5iJ6kL7m; // string | The unique entitlement ID.

try {
    $result = $apiInstance->entitlementsDelete($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EntitlementsApi->entitlementsDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The unique entitlement ID. | |

### Return type

[**\Solifyn\Model\EntitlementDetailResponseDto**](../Model/EntitlementDetailResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `entitlementsGet()`

```php
entitlementsGet($id): \Solifyn\Model\EntitlementDetailResponseDto
```

Retrieve Entitlement

Retrieve a specific entitlement definition by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\EntitlementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = ent_8Z1aB2cD3eF4gH5iJ6kL7m; // string | The unique entitlement ID.

try {
    $result = $apiInstance->entitlementsGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EntitlementsApi->entitlementsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The unique entitlement ID. | |

### Return type

[**\Solifyn\Model\EntitlementDetailResponseDto**](../Model/EntitlementDetailResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `entitlementsList()`

```php
entitlementsList(): \Solifyn\Model\EntitlementDetailResponseDto[]
```

List Entitlements

List all independent entitlements for the active business.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\EntitlementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->entitlementsList();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EntitlementsApi->entitlementsList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Solifyn\Model\EntitlementDetailResponseDto[]**](../Model/EntitlementDetailResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `entitlementsUpdate()`

```php
entitlementsUpdate($id, $update_entitlement_dto): \Solifyn\Model\EntitlementDetailResponseDto
```

Update Entitlement

Update details of an existing independent entitlement.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\EntitlementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = ent_8Z1aB2cD3eF4gH5iJ6kL7m; // string | The unique entitlement ID.
$update_entitlement_dto = new \Solifyn\Model\UpdateEntitlementDto(); // \Solifyn\Model\UpdateEntitlementDto

try {
    $result = $apiInstance->entitlementsUpdate($id, $update_entitlement_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EntitlementsApi->entitlementsUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The unique entitlement ID. | |
| **update_entitlement_dto** | [**\Solifyn\Model\UpdateEntitlementDto**](../Model/UpdateEntitlementDto.md)|  | |

### Return type

[**\Solifyn\Model\EntitlementDetailResponseDto**](../Model/EntitlementDetailResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
