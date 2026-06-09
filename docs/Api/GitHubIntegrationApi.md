# Solifyn\GitHubIntegrationApi

All URIs are relative to https://api.solifyn.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**githubGetInstallUrl()**](GitHubIntegrationApi.md#githubGetInstallUrl) | **GET** /v1/github/install | Get GitHub App Installation URL |
| [**githubListRepos()**](GitHubIntegrationApi.md#githubListRepos) | **GET** /v1/github/repos | List Available GitHub Repositories |


## `githubGetInstallUrl()`

```php
githubGetInstallUrl($product_id)
```

Get GitHub App Installation URL

Generates the URL to install the system-wide GitHub App onto the merchant's GitHub account/org.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\GitHubIntegrationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$product_id = 'product_id_example'; // string | Optional Product ID to redirect back to after installation

try {
    $apiInstance->githubGetInstallUrl($product_id);
} catch (Exception $e) {
    echo 'Exception when calling GitHubIntegrationApi->githubGetInstallUrl: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **product_id** | **string**| Optional Product ID to redirect back to after installation | [optional] |

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

## `githubListRepos()`

```php
githubListRepos(): \Solifyn\Model\GithubReposResponseDto[]
```

List Available GitHub Repositories

Retrieves all repositories accessible by the merchant's installed GitHub App.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\GitHubIntegrationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->githubListRepos();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GitHubIntegrationApi->githubListRepos: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Solifyn\Model\GithubReposResponseDto[]**](../Model/GithubReposResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
