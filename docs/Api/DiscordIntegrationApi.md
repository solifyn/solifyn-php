# Solifyn\DiscordIntegrationApi

All URIs are relative to https://api.solifyn.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**discordGetInstallUrl()**](DiscordIntegrationApi.md#discordGetInstallUrl) | **GET** /v1/discord/install | Get Discord Bot Installation URL |
| [**discordListRoles()**](DiscordIntegrationApi.md#discordListRoles) | **GET** /v1/discord/roles | List Guild Discord Roles |


## `discordGetInstallUrl()`

```php
discordGetInstallUrl($product_id)
```

Get Discord Bot Installation URL

Generates the URL to invite the system-wide Discord Bot onto the merchant's Discord server.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\DiscordIntegrationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$product_id = 'product_id_example'; // string | Optional Product ID to redirect back to after installation

try {
    $apiInstance->discordGetInstallUrl($product_id);
} catch (Exception $e) {
    echo 'Exception when calling DiscordIntegrationApi->discordGetInstallUrl: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **product_id** | **string**| Optional Product ID to redirect back to after installation | [optional] |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `discordListRoles()`

```php
discordListRoles(): \Solifyn\Model\DiscordRolesResponseDto[]
```

List Guild Discord Roles

Retrieves all roles available in the connected merchant's Discord server/guild.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Solifyn\Api\DiscordIntegrationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->discordListRoles();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DiscordIntegrationApi->discordListRoles: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Solifyn\Model\DiscordRolesResponseDto[]**](../Model/DiscordRolesResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
