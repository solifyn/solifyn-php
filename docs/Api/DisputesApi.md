# Solifyn\DisputesApi

All URIs are relative to https://api.solifyn.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**disputesGenerateReport()**](DisputesApi.md#disputesGenerateReport) | **GET** /v1/transactions/disputes/report | Generate Dispute CSV Report |
| [**disputesGet()**](DisputesApi.md#disputesGet) | **GET** /v1/transactions/disputes/{id} | Retrieve Dispute |
| [**disputesList()**](DisputesApi.md#disputesList) | **GET** /v1/transactions/disputes | List Disputes |
| [**disputesSubmitEvidence()**](DisputesApi.md#disputesSubmitEvidence) | **POST** /v1/transactions/disputes/{id}/submit | Submit Dispute Evidence |
| [**disputesUpdateEvidence()**](DisputesApi.md#disputesUpdateEvidence) | **PATCH** /v1/transactions/disputes/{id}/evidence | Update Dispute Evidence |
| [**disputesUploadEvidenceFile()**](DisputesApi.md#disputesUploadEvidenceFile) | **POST** /v1/transactions/disputes/upload | Upload Evidence File |


## `disputesGenerateReport()`

```php
disputesGenerateReport($created_at_gte, $created_at_lte, $status)
```

Generate Dispute CSV Report

Generates a downloadable CSV report of disputes matching the filters.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\DisputesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$created_at_gte = 'created_at_gte_example'; // string | Filter disputes created after this ISO date-time string
$created_at_lte = 'created_at_lte_example'; // string | Filter disputes created before this ISO date-time string
$status = 'status_example'; // string | Filter disputes by status

try {
    $apiInstance->disputesGenerateReport($created_at_gte, $created_at_lte, $status);
} catch (Exception $e) {
    echo 'Exception when calling DisputesApi->disputesGenerateReport: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **created_at_gte** | **string**| Filter disputes created after this ISO date-time string | [optional] |
| **created_at_lte** | **string**| Filter disputes created before this ISO date-time string | [optional] |
| **status** | **string**| Filter disputes by status | [optional] |

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

## `disputesGet()`

```php
disputesGet($id): \Solifyn\Model\Dispute
```

Retrieve Dispute

Retrieve details of a specific dispute by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\DisputesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = dsp_123; // string | The dispute ID

try {
    $result = $apiInstance->disputesGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DisputesApi->disputesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The dispute ID | |

### Return type

[**\Solifyn\Model\Dispute**](../Model/Dispute.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `disputesList()`

```php
disputesList($page, $limit, $status, $type): \Solifyn\Model\DisputeList
```

List Disputes

Retrieve disputes associated with the active business.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\DisputesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // string | Page number for pagination
$limit = 10; // string | Page size limit for pagination
$status = 'status_example'; // string | Filter disputes by status
$type = 'type_example'; // string | Filter by type: dispute or alert

try {
    $result = $apiInstance->disputesList($page, $limit, $status, $type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DisputesApi->disputesList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **string**| Page number for pagination | [optional] |
| **limit** | **string**| Page size limit for pagination | [optional] |
| **status** | **string**| Filter disputes by status | [optional] |
| **type** | **string**| Filter by type: dispute or alert | [optional] |

### Return type

[**\Solifyn\Model\DisputeList**](../Model/DisputeList.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `disputesSubmitEvidence()`

```php
disputesSubmitEvidence($id): \Solifyn\Model\Dispute
```

Submit Dispute Evidence

Finalize and submit the uploaded evidence for review.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\DisputesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = dsp_123; // string | The dispute ID

try {
    $result = $apiInstance->disputesSubmitEvidence($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DisputesApi->disputesSubmitEvidence: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The dispute ID | |

### Return type

[**\Solifyn\Model\Dispute**](../Model/Dispute.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `disputesUpdateEvidence()`

```php
disputesUpdateEvidence($id, $dispute_evidence_update): \Solifyn\Model\Dispute
```

Update Dispute Evidence

Upload and update evidence attachments for a dispute.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\DisputesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = dsp_123; // string | The dispute ID
$dispute_evidence_update = new \Solifyn\Model\DisputeEvidenceUpdate(); // \Solifyn\Model\DisputeEvidenceUpdate

try {
    $result = $apiInstance->disputesUpdateEvidence($id, $dispute_evidence_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DisputesApi->disputesUpdateEvidence: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The dispute ID | |
| **dispute_evidence_update** | [**\Solifyn\Model\DisputeEvidenceUpdate**](../Model/DisputeEvidenceUpdate.md)|  | |

### Return type

[**\Solifyn\Model\Dispute**](../Model/Dispute.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `disputesUploadEvidenceFile()`

```php
disputesUploadEvidenceFile($file): \Solifyn\Model\DisputeFileUpload
```

Upload Evidence File

Upload a support file (image, PDF, video) to use as dispute evidence.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\DisputesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$file = '/path/to/file.txt'; // \SplFileObject | The evidence file to upload (Max 25MB: JPEG, PNG, GIF, WEBP, PDF, MP4, WEBM, QuickTime)

try {
    $result = $apiInstance->disputesUploadEvidenceFile($file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DisputesApi->disputesUploadEvidenceFile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **file** | **\SplFileObject****\SplFileObject**| The evidence file to upload (Max 25MB: JPEG, PNG, GIF, WEBP, PDF, MP4, WEBM, QuickTime) | |

### Return type

[**\Solifyn\Model\DisputeFileUpload**](../Model/DisputeFileUpload.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
