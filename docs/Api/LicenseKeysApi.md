# Solifyn\LicenseKeysApi

All URIs are relative to https://api.solifyn.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**licensesCreate()**](LicenseKeysApi.md#licensesCreate) | **POST** /v1/licenses | Create License Key |
| [**licensesDeleteInstance()**](LicenseKeysApi.md#licensesDeleteInstance) | **DELETE** /v1/licenses/instances/{instanceId} | Force Delete Instance |
| [**licensesGet()**](LicenseKeysApi.md#licensesGet) | **GET** /v1/licenses/{id} | Get License Key |
| [**licensesGetInstance()**](LicenseKeysApi.md#licensesGetInstance) | **GET** /v1/licenses/{id}/instances/{instanceId} | Get License Key Instance |
| [**licensesGetInstances()**](LicenseKeysApi.md#licensesGetInstances) | **GET** /v1/licenses/{id}/instances | Get License Key Instances |
| [**licensesList()**](LicenseKeysApi.md#licensesList) | **GET** /v1/licenses | List License Keys |
| [**licensesToggle()**](LicenseKeysApi.md#licensesToggle) | **POST** /v1/licenses/{id}/toggle | Toggle License Status |
| [**licensesUpdate()**](LicenseKeysApi.md#licensesUpdate) | **PATCH** /v1/licenses/{id} | Update License Key |
| [**licensesUpdateInstance()**](LicenseKeysApi.md#licensesUpdateInstance) | **PATCH** /v1/licenses/{id}/instances/{instanceId} | Update License Key Instance |
| [**licensesUpdateInstancePost()**](LicenseKeysApi.md#licensesUpdateInstancePost) | **POST** /v1/licenses/{id}/instances/{instanceId} | Update License Key Instance (POST) |


## `licensesCreate()`

```php
licensesCreate($licenses_create_request): \Solifyn\Model\License
```

Create License Key

Manually issue a new license key for a specific product.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\LicenseKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$licenses_create_request = new \Solifyn\Model\LicensesCreateRequest(); // \Solifyn\Model\LicensesCreateRequest

try {
    $result = $apiInstance->licensesCreate($licenses_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LicenseKeysApi->licensesCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **licenses_create_request** | [**\Solifyn\Model\LicensesCreateRequest**](../Model/LicensesCreateRequest.md)|  | |

### Return type

[**\Solifyn\Model\License**](../Model/License.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `licensesDeleteInstance()`

```php
licensesDeleteInstance($instance_id): \Solifyn\Model\Instance
```

Force Delete Instance

Administrative endpoint to force-delete an instance globally by its database ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\LicenseKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$instance_id = inc_123; // string | The unique hardware activation instance ID.

try {
    $result = $apiInstance->licensesDeleteInstance($instance_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LicenseKeysApi->licensesDeleteInstance: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **instance_id** | **string**| The unique hardware activation instance ID. | |

### Return type

[**\Solifyn\Model\Instance**](../Model/Instance.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `licensesGet()`

```php
licensesGet($id): \Solifyn\Model\License
```

Get License Key

Retrieve complete administrative details of a specific license key.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\LicenseKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The unique license key ID.

try {
    $result = $apiInstance->licensesGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LicenseKeysApi->licensesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The unique license key ID. | |

### Return type

[**\Solifyn\Model\License**](../Model/License.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `licensesGetInstance()`

```php
licensesGetInstance($id, $instance_id): \Solifyn\Model\Instance
```

Get License Key Instance

Retrieve administrative details of a specific software license instance.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\LicenseKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The unique administrative identifier (ID) of the parent license key.
$instance_id = inc_123; // string | The client-generated instance ID (hardware hash) or the internal database ID of the instance.

try {
    $result = $apiInstance->licensesGetInstance($id, $instance_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LicenseKeysApi->licensesGetInstance: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The unique administrative identifier (ID) of the parent license key. | |
| **instance_id** | **string**| The client-generated instance ID (hardware hash) or the internal database ID of the instance. | |

### Return type

[**\Solifyn\Model\Instance**](../Model/Instance.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `licensesGetInstances()`

```php
licensesGetInstances($id): \Solifyn\Model\Instance[]
```

Get License Key Instances

Retrieve all active devices/instances for a specific administrative license key.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\LicenseKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = lic_123; // string | The unique administrative identifier (ID) of the parent license key.

try {
    $result = $apiInstance->licensesGetInstances($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LicenseKeysApi->licensesGetInstances: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The unique administrative identifier (ID) of the parent license key. | |

### Return type

[**\Solifyn\Model\Instance[]**](../Model/Instance.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `licensesList()`

```php
licensesList(): \Solifyn\Model\License[]
```

List License Keys

List all administrative license keys belonging to products under your active business.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\LicenseKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->licensesList();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LicenseKeysApi->licensesList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Solifyn\Model\License[]**](../Model/License.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `licensesToggle()`

```php
licensesToggle($id): \Solifyn\Model\License
```

Toggle License Status

Toggle the status of a specific license key between ACTIVE and DISABLED.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\LicenseKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = lic_123; // string | The unique license key ID.

try {
    $result = $apiInstance->licensesToggle($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LicenseKeysApi->licensesToggle: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The unique license key ID. | |

### Return type

[**\Solifyn\Model\License**](../Model/License.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `licensesUpdate()`

```php
licensesUpdate($id, $licenses_update_request): \Solifyn\Model\License
```

Update License Key

Update limits or status of an existing license key.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\LicenseKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The unique license key ID.
$licenses_update_request = new \Solifyn\Model\LicensesUpdateRequest(); // \Solifyn\Model\LicensesUpdateRequest

try {
    $result = $apiInstance->licensesUpdate($id, $licenses_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LicenseKeysApi->licensesUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The unique license key ID. | |
| **licenses_update_request** | [**\Solifyn\Model\LicensesUpdateRequest**](../Model/LicensesUpdateRequest.md)|  | |

### Return type

[**\Solifyn\Model\License**](../Model/License.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `licensesUpdateInstance()`

```php
licensesUpdateInstance($instance_id, $id, $licenses_update_instance_post_request): \Solifyn\Model\Instance
```

Update License Key Instance

Update administrative details (like friendly display name or custom IP) of an active license device instance.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\LicenseKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$instance_id = inc_123; // string | The client-generated instance ID (hardware hash) or the internal database ID of the instance.
$id = 'id_example'; // string | The unique administrative identifier (ID) of the parent license key.
$licenses_update_instance_post_request = new \Solifyn\Model\LicensesUpdateInstancePostRequest(); // \Solifyn\Model\LicensesUpdateInstancePostRequest

try {
    $result = $apiInstance->licensesUpdateInstance($instance_id, $id, $licenses_update_instance_post_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LicenseKeysApi->licensesUpdateInstance: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **instance_id** | **string**| The client-generated instance ID (hardware hash) or the internal database ID of the instance. | |
| **id** | **string**| The unique administrative identifier (ID) of the parent license key. | |
| **licenses_update_instance_post_request** | [**\Solifyn\Model\LicensesUpdateInstancePostRequest**](../Model/LicensesUpdateInstancePostRequest.md)|  | |

### Return type

[**\Solifyn\Model\Instance**](../Model/Instance.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `licensesUpdateInstancePost()`

```php
licensesUpdateInstancePost($instance_id, $id, $licenses_update_instance_post_request): \Solifyn\Model\Instance
```

Update License Key Instance (POST)

Alternative POST endpoint to update administrative details (like friendly display name or custom IP) of an active license device instance.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\LicenseKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$instance_id = inc_123; // string | The client-generated instance ID (hardware hash) or the internal database ID of the instance.
$id = 'id_example'; // string | The unique administrative identifier (ID) of the parent license key.
$licenses_update_instance_post_request = new \Solifyn\Model\LicensesUpdateInstancePostRequest(); // \Solifyn\Model\LicensesUpdateInstancePostRequest

try {
    $result = $apiInstance->licensesUpdateInstancePost($instance_id, $id, $licenses_update_instance_post_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LicenseKeysApi->licensesUpdateInstancePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **instance_id** | **string**| The client-generated instance ID (hardware hash) or the internal database ID of the instance. | |
| **id** | **string**| The unique administrative identifier (ID) of the parent license key. | |
| **licenses_update_instance_post_request** | [**\Solifyn\Model\LicensesUpdateInstancePostRequest**](../Model/LicensesUpdateInstancePostRequest.md)|  | |

### Return type

[**\Solifyn\Model\Instance**](../Model/Instance.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
