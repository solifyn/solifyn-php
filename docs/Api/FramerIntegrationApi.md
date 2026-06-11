# Solifyn\FramerIntegrationApi

All URIs are relative to https://api.solifyn.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**framerCreateTemplate()**](FramerIntegrationApi.md#framerCreateTemplate) | **POST** /v1/framer/templates | Create Framer Template |
| [**framerDeleteTemplate()**](FramerIntegrationApi.md#framerDeleteTemplate) | **DELETE** /v1/framer/templates/{id} | Delete Framer Template |
| [**framerGetTemplate()**](FramerIntegrationApi.md#framerGetTemplate) | **GET** /v1/framer/templates/{id} | Retrieve Framer Template |
| [**framerListTemplates()**](FramerIntegrationApi.md#framerListTemplates) | **GET** /v1/framer/templates | List Framer Templates |
| [**framerUpdateTemplate()**](FramerIntegrationApi.md#framerUpdateTemplate) | **PUT** /v1/framer/templates/{id} | Update Framer Template |


## `framerCreateTemplate()`

```php
framerCreateTemplate($create_framer_template_dto): \Solifyn\Model\FramerTemplateResponseDto
```

Create Framer Template

Registers a new Framer template with its public remix link for the active business.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\FramerIntegrationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_framer_template_dto = new \Solifyn\Model\CreateFramerTemplateDto(); // \Solifyn\Model\CreateFramerTemplateDto

try {
    $result = $apiInstance->framerCreateTemplate($create_framer_template_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FramerIntegrationApi->framerCreateTemplate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_framer_template_dto** | [**\Solifyn\Model\CreateFramerTemplateDto**](../Model/CreateFramerTemplateDto.md)|  | |

### Return type

[**\Solifyn\Model\FramerTemplateResponseDto**](../Model/FramerTemplateResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `framerDeleteTemplate()`

```php
framerDeleteTemplate($id)
```

Delete Framer Template

Deletes a registered Framer template for the active business.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\FramerIntegrationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The Framer template ID

try {
    $apiInstance->framerDeleteTemplate($id);
} catch (Exception $e) {
    echo 'Exception when calling FramerIntegrationApi->framerDeleteTemplate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The Framer template ID | |

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

## `framerGetTemplate()`

```php
framerGetTemplate($id): \Solifyn\Model\FramerTemplateResponseDto
```

Retrieve Framer Template

Retrieves details of a specific registered Framer template.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\FramerIntegrationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The Framer template ID

try {
    $result = $apiInstance->framerGetTemplate($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FramerIntegrationApi->framerGetTemplate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The Framer template ID | |

### Return type

[**\Solifyn\Model\FramerTemplateResponseDto**](../Model/FramerTemplateResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `framerListTemplates()`

```php
framerListTemplates(): \Solifyn\Model\FramerTemplateResponseDto[]
```

List Framer Templates

Retrieves all registered Framer templates for the active business.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\FramerIntegrationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->framerListTemplates();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FramerIntegrationApi->framerListTemplates: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Solifyn\Model\FramerTemplateResponseDto[]**](../Model/FramerTemplateResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `framerUpdateTemplate()`

```php
framerUpdateTemplate($id, $update_framer_template_dto): \Solifyn\Model\FramerTemplateResponseDto
```

Update Framer Template

Updates a registered Framer template for the active business.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\FramerIntegrationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The Framer template ID
$update_framer_template_dto = new \Solifyn\Model\UpdateFramerTemplateDto(); // \Solifyn\Model\UpdateFramerTemplateDto

try {
    $result = $apiInstance->framerUpdateTemplate($id, $update_framer_template_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FramerIntegrationApi->framerUpdateTemplate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The Framer template ID | |
| **update_framer_template_dto** | [**\Solifyn\Model\UpdateFramerTemplateDto**](../Model/UpdateFramerTemplateDto.md)|  | |

### Return type

[**\Solifyn\Model\FramerTemplateResponseDto**](../Model/FramerTemplateResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
