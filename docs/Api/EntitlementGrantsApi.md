# Solifyn\EntitlementGrantsApi

All URIs are relative to https://api.solifyn.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**entitlementGrantsGet()**](EntitlementGrantsApi.md#entitlementGrantsGet) | **GET** /v1/entitlement-grants/{id} | Retrieve Entitlement Grant |
| [**entitlementGrantsList()**](EntitlementGrantsApi.md#entitlementGrantsList) | **GET** /v1/entitlement-grants | List Entitlement Grants |
| [**entitlementGrantsRetry()**](EntitlementGrantsApi.md#entitlementGrantsRetry) | **POST** /v1/entitlement-grants/{id}/retry | Retry Entitlement Grant Delivery |
| [**entitlementGrantsRevoke()**](EntitlementGrantsApi.md#entitlementGrantsRevoke) | **POST** /v1/entitlement-grants/{id}/revoke | Manually Revoke Entitlement Grant |


## `entitlementGrantsGet()`

```php
entitlementGrantsGet($id): \Solifyn\Model\EntitlementGrantResponseDto
```

Retrieve Entitlement Grant

Retrieve details of a specific entitlement grant.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\EntitlementGrantsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The unique grant ID

try {
    $result = $apiInstance->entitlementGrantsGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EntitlementGrantsApi->entitlementGrantsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The unique grant ID | |

### Return type

[**\Solifyn\Model\EntitlementGrantResponseDto**](../Model/EntitlementGrantResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `entitlementGrantsList()`

```php
entitlementGrantsList($status, $entitlement_id, $product_id): \Solifyn\Model\EntitlementGrantResponseDto[]
```

List Entitlement Grants

Retrieve all GitHub repository entitlement grants for the active business.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\EntitlementGrantsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$status = 'status_example'; // string | Filter by status (PENDING, DELIVERED, FAILED, REVOKED)
$entitlement_id = 'entitlement_id_example'; // string | Filter by entitlement config ID
$product_id = 'product_id_example'; // string | Filter by product ID

try {
    $result = $apiInstance->entitlementGrantsList($status, $entitlement_id, $product_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EntitlementGrantsApi->entitlementGrantsList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **status** | **string**| Filter by status (PENDING, DELIVERED, FAILED, REVOKED) | [optional] |
| **entitlement_id** | **string**| Filter by entitlement config ID | [optional] |
| **product_id** | **string**| Filter by product ID | [optional] |

### Return type

[**\Solifyn\Model\EntitlementGrantResponseDto[]**](../Model/EntitlementGrantResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `entitlementGrantsRetry()`

```php
entitlementGrantsRetry($id): \Solifyn\Model\EntitlementGrantResponseDto
```

Retry Entitlement Grant Delivery

Attempts to re-invite the collaborator if GitHub username is already connected, or resets the OAuth URL redirect.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\EntitlementGrantsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The unique grant ID

try {
    $result = $apiInstance->entitlementGrantsRetry($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EntitlementGrantsApi->entitlementGrantsRetry: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The unique grant ID | |

### Return type

[**\Solifyn\Model\EntitlementGrantResponseDto**](../Model/EntitlementGrantResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `entitlementGrantsRevoke()`

```php
entitlementGrantsRevoke($id): \Solifyn\Model\EntitlementGrantResponseDto
```

Manually Revoke Entitlement Grant

Manually remove the customer collaborator access from the repository and revoke the grant.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\EntitlementGrantsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The unique grant ID

try {
    $result = $apiInstance->entitlementGrantsRevoke($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EntitlementGrantsApi->entitlementGrantsRevoke: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The unique grant ID | |

### Return type

[**\Solifyn\Model\EntitlementGrantResponseDto**](../Model/EntitlementGrantResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
