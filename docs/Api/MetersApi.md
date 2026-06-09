# Solifyn\MetersApi

All URIs are relative to https://api.solifyn.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**eventsIngest()**](MetersApi.md#eventsIngest) | **POST** /v1/meters/ingest | Ingest Events |
| [**metersCreate()**](MetersApi.md#metersCreate) | **POST** /v1/meters | Create Meter |
| [**metersGet()**](MetersApi.md#metersGet) | **GET** /v1/meters/{id} | Retrieve Meter |
| [**metersGetEvents()**](MetersApi.md#metersGetEvents) | **GET** /v1/meters/{id}/events | List Meter Events |
| [**metersGetQuantities()**](MetersApi.md#metersGetQuantities) | **GET** /v1/meters/{id}/quantities | Get Meter Quantities |
| [**metersList()**](MetersApi.md#metersList) | **GET** /v1/meters | List Meters |
| [**metersUpdate()**](MetersApi.md#metersUpdate) | **PATCH** /v1/meters/{id} | Update Meter |


## `eventsIngest()`

```php
eventsIngest($meter_ingest_request_dto): \Solifyn\Model\MeterIngestResponseDto
```

Ingest Events

Ingest usage events for meters.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\MetersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$meter_ingest_request_dto = new \Solifyn\Model\MeterIngestRequestDto(); // \Solifyn\Model\MeterIngestRequestDto

try {
    $result = $apiInstance->eventsIngest($meter_ingest_request_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetersApi->eventsIngest: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **meter_ingest_request_dto** | [**\Solifyn\Model\MeterIngestRequestDto**](../Model/MeterIngestRequestDto.md)|  | |

### Return type

[**\Solifyn\Model\MeterIngestResponseDto**](../Model/MeterIngestResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `metersCreate()`

```php
metersCreate($create_meter_dto): \Solifyn\Model\MeterResponseDto
```

Create Meter

Create a new usage meter for event-based billing and usage tracking.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\MetersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_meter_dto = new \Solifyn\Model\CreateMeterDto(); // \Solifyn\Model\CreateMeterDto

try {
    $result = $apiInstance->metersCreate($create_meter_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetersApi->metersCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_meter_dto** | [**\Solifyn\Model\CreateMeterDto**](../Model/CreateMeterDto.md)|  | |

### Return type

[**\Solifyn\Model\MeterResponseDto**](../Model/MeterResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `metersGet()`

```php
metersGet($id, $start_date, $end_date): \Solifyn\Model\MeterDetailResponseDto
```

Retrieve Meter

Retrieve a meter and its most recent usage events.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\MetersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = mtr_8Z1aB2cD3eF4gH5iJ6kL7m; // string | The unique meter ID.
$start_date = 'start_date_example'; // string
$end_date = 'end_date_example'; // string

try {
    $result = $apiInstance->metersGet($id, $start_date, $end_date);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetersApi->metersGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The unique meter ID. | |
| **start_date** | **string**|  | |
| **end_date** | **string**|  | |

### Return type

[**\Solifyn\Model\MeterDetailResponseDto**](../Model/MeterDetailResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `metersGetEvents()`

```php
metersGetEvents($id, $limit): \Solifyn\Model\MeterEventsResponseDto
```

List Meter Events

List recent usage events recorded for a meter.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\MetersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = mtr_8Z1aB2cD3eF4gH5iJ6kL7m; // string | The unique meter ID.
$limit = 100; // float | Maximum number of usage events to return.

try {
    $result = $apiInstance->metersGetEvents($id, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetersApi->metersGetEvents: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The unique meter ID. | |
| **limit** | **float**| Maximum number of usage events to return. | [optional] [default to 100] |

### Return type

[**\Solifyn\Model\MeterEventsResponseDto**](../Model/MeterEventsResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `metersGetQuantities()`

```php
metersGetQuantities($id, $start_date, $end_date): \Solifyn\Model\MeterQuantitiesResponseDto
```

Get Meter Quantities

Get aggregated usage quantities for a meter within an optional date range.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\MetersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = mtr_8Z1aB2cD3eF4gH5iJ6kL7m; // string | The unique meter ID.
$start_date = 'start_date_example'; // string | Inclusive start date in ISO 8601 format.
$end_date = 'end_date_example'; // string | Inclusive end date in ISO 8601 format.

try {
    $result = $apiInstance->metersGetQuantities($id, $start_date, $end_date);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetersApi->metersGetQuantities: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The unique meter ID. | |
| **start_date** | **string**| Inclusive start date in ISO 8601 format. | [optional] |
| **end_date** | **string**| Inclusive end date in ISO 8601 format. | [optional] |

### Return type

[**\Solifyn\Model\MeterQuantitiesResponseDto**](../Model/MeterQuantitiesResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `metersList()`

```php
metersList($status): \Solifyn\Model\MeterResponseDto[]
```

List Meters

List meters belonging to your active business. You can filter by archived status.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\MetersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$status = 'status_example'; // string | Filter by meter status.

try {
    $result = $apiInstance->metersList($status);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetersApi->metersList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **status** | **string**| Filter by meter status. | [optional] |

### Return type

[**\Solifyn\Model\MeterResponseDto[]**](../Model/MeterResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `metersUpdate()`

```php
metersUpdate($id, $update_meter_dto): \Solifyn\Model\MeterResponseDto
```

Update Meter

Update an existing meter definition.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\MetersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = mtr_8Z1aB2cD3eF4gH5iJ6kL7m; // string | The unique meter ID.
$update_meter_dto = new \Solifyn\Model\UpdateMeterDto(); // \Solifyn\Model\UpdateMeterDto

try {
    $result = $apiInstance->metersUpdate($id, $update_meter_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetersApi->metersUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The unique meter ID. | |
| **update_meter_dto** | [**\Solifyn\Model\UpdateMeterDto**](../Model/UpdateMeterDto.md)|  | |

### Return type

[**\Solifyn\Model\MeterResponseDto**](../Model/MeterResponseDto.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
