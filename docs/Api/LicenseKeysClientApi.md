# Solifyn\LicenseKeysClientApi

All URIs are relative to https://api.solifyn.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**licensesActivate()**](LicenseKeysClientApi.md#licensesActivate) | **POST** /v1/licenses/activate | Activate License Key |
| [**licensesDeactivate()**](LicenseKeysClientApi.md#licensesDeactivate) | **POST** /v1/licenses/deactivate/{instanceId} | Deactivate Instance |
| [**licensesInstances()**](LicenseKeysClientApi.md#licensesInstances) | **GET** /v1/licenses/instances/{licenseId} | Get Active Instances |
| [**licensesVerify()**](LicenseKeysClientApi.md#licensesVerify) | **POST** /v1/licenses/verify | Validate License Key |


## `licensesActivate()`

```php
licensesActivate($licenses_activate_request): \Solifyn\Model\Instance
```

Activate License Key

Register and activate a device or instance for a specific license key.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\LicenseKeysClientApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$licenses_activate_request = new \Solifyn\Model\LicensesActivateRequest(); // \Solifyn\Model\LicensesActivateRequest

try {
    $result = $apiInstance->licensesActivate($licenses_activate_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LicenseKeysClientApi->licensesActivate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **licenses_activate_request** | [**\Solifyn\Model\LicensesActivateRequest**](../Model/LicensesActivateRequest.md)|  | |

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

## `licensesDeactivate()`

```php
licensesDeactivate($instance_id, $licenses_deactivate_request): \Solifyn\Model\LicensesDeactivate200Response
```

Deactivate Instance

Deactivate or unregister an active device instance from a license key.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\LicenseKeysClientApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$instance_id = 'instance_id_example'; // string | The unique device instance ID.
$licenses_deactivate_request = new \Solifyn\Model\LicensesDeactivateRequest(); // \Solifyn\Model\LicensesDeactivateRequest

try {
    $result = $apiInstance->licensesDeactivate($instance_id, $licenses_deactivate_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LicenseKeysClientApi->licensesDeactivate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **instance_id** | **string**| The unique device instance ID. | |
| **licenses_deactivate_request** | [**\Solifyn\Model\LicensesDeactivateRequest**](../Model/LicensesDeactivateRequest.md)|  | |

### Return type

[**\Solifyn\Model\LicensesDeactivate200Response**](../Model/LicensesDeactivate200Response.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `licensesInstances()`

```php
licensesInstances($license_id): \Solifyn\Model\Instance[]
```

Get Active Instances

List all active devices or server instances linked to a specific license key.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\LicenseKeysClientApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$license_id = 'license_id_example'; // string | The unique license key ID.

try {
    $result = $apiInstance->licensesInstances($license_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LicenseKeysClientApi->licensesInstances: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **license_id** | **string**| The unique license key ID. | |

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

## `licensesVerify()`

```php
licensesVerify($licenses_verify_request): \Solifyn\Model\LicenseValidationResponse
```

Validate License Key

Verify if a software license key is valid, active, and has not exceeded its limits.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\LicenseKeysClientApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$licenses_verify_request = new \Solifyn\Model\LicensesVerifyRequest(); // \Solifyn\Model\LicensesVerifyRequest

try {
    $result = $apiInstance->licensesVerify($licenses_verify_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LicenseKeysClientApi->licensesVerify: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **licenses_verify_request** | [**\Solifyn\Model\LicensesVerifyRequest**](../Model/LicensesVerifyRequest.md)|  | |

### Return type

[**\Solifyn\Model\LicenseValidationResponse**](../Model/LicenseValidationResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
