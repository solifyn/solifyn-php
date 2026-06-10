# Solifyn\CustomersApi

All URIs are relative to https://api.solifyn.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**customersCreate()**](CustomersApi.md#customersCreate) | **POST** /v1/customers | Create Customer |
| [**customersGenerateInvite()**](CustomersApi.md#customersGenerateInvite) | **POST** /v1/customers/{id}/share | Generate Shared Invite |
| [**customersGet()**](CustomersApi.md#customersGet) | **GET** /v1/customers/{id} | Retrieve Customer |
| [**customersList()**](CustomersApi.md#customersList) | **GET** /v1/customers | List Customers |
| [**customersUpdate()**](CustomersApi.md#customersUpdate) | **PATCH** /v1/customers/{id} | Update Customer |


## `customersCreate()`

```php
customersCreate($create_customer_dto): \Solifyn\Model\CustomerResponseDto
```

Create Customer

Add/upsert a new customer profile under the current business context.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\CustomersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_customer_dto = new \Solifyn\Model\CreateCustomerDto(); // \Solifyn\Model\CreateCustomerDto

try {
    $result = $apiInstance->customersCreate($create_customer_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomersApi->customersCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_customer_dto** | [**\Solifyn\Model\CreateCustomerDto**](../Model/CreateCustomerDto.md)|  | |

### Return type

[**\Solifyn\Model\CustomerResponseDto**](../Model/CustomerResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `customersGenerateInvite()`

```php
customersGenerateInvite($id): \Solifyn\Model\CustomerSharedInviteResponseDto
```

Generate Shared Invite

Generate a short-lived token granting temporary customer self-service billing page access.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\CustomersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = user_123; // string | Customer ID

try {
    $result = $apiInstance->customersGenerateInvite($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomersApi->customersGenerateInvite: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Customer ID | |

### Return type

[**\Solifyn\Model\CustomerSharedInviteResponseDto**](../Model/CustomerSharedInviteResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `customersGet()`

```php
customersGet($id): \Solifyn\Model\CustomerResponseDto
```

Retrieve Customer

Retrieve details of a customer profile by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\CustomersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = user_123; // string | Customer ID

try {
    $result = $apiInstance->customersGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomersApi->customersGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Customer ID | |

### Return type

[**\Solifyn\Model\CustomerResponseDto**](../Model/CustomerResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `customersList()`

```php
customersList(): \Solifyn\Model\CustomerListResponseDto
```

List Customers

Retrieve all customers associated with the current active business.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\CustomersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->customersList();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomersApi->customersList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Solifyn\Model\CustomerListResponseDto**](../Model/CustomerListResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `customersUpdate()`

```php
customersUpdate($id, $update_customer_dto): \Solifyn\Model\CustomerMessageResponseDto
```

Update Customer

Update name, phone, or metadata of an existing customer profile.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\CustomersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = user_123; // string | Customer ID
$update_customer_dto = new \Solifyn\Model\UpdateCustomerDto(); // \Solifyn\Model\UpdateCustomerDto

try {
    $result = $apiInstance->customersUpdate($id, $update_customer_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomersApi->customersUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Customer ID | |
| **update_customer_dto** | [**\Solifyn\Model\UpdateCustomerDto**](../Model/UpdateCustomerDto.md)|  | |

### Return type

[**\Solifyn\Model\CustomerMessageResponseDto**](../Model/CustomerMessageResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
