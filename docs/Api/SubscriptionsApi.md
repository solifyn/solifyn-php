# Solifyn\SubscriptionsApi

All URIs are relative to https://api.solifyn.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**subscriptionsAction()**](SubscriptionsApi.md#subscriptionsAction) | **POST** /v1/subscriptions/{subscriptionId}/{action} | Subscription Action |
| [**subscriptionsGet()**](SubscriptionsApi.md#subscriptionsGet) | **GET** /v1/subscriptions/{id} | Retrieve Subscription Details |
| [**subscriptionsList()**](SubscriptionsApi.md#subscriptionsList) | **GET** /v1/subscriptions | List Subscriptions |


## `subscriptionsAction()`

```php
subscriptionsAction($subscription_id, $action, $subscription_action): \Solifyn\Model\SubscriptionsAction201Response
```

Subscription Action

Cancel, pause, resume, or add free days to a customer subscription.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\SubscriptionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$subscription_id = mem_123; // string | The customer subscription ID
$action = 'action_example'; // string | The subscription task to execute
$subscription_action = new \Solifyn\Model\SubscriptionAction(); // \Solifyn\Model\SubscriptionAction

try {
    $result = $apiInstance->subscriptionsAction($subscription_id, $action, $subscription_action);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubscriptionsApi->subscriptionsAction: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **subscription_id** | **string**| The customer subscription ID | |
| **action** | **string**| The subscription task to execute | |
| **subscription_action** | [**\Solifyn\Model\SubscriptionAction**](../Model/SubscriptionAction.md)|  | |

### Return type

[**\Solifyn\Model\SubscriptionsAction201Response**](../Model/SubscriptionsAction201Response.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `subscriptionsGet()`

```php
subscriptionsGet($id): \Solifyn\Model\SubscriptionDetail
```

Retrieve Subscription Details

Retrieve detailed information about a subscription and its billing history.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\SubscriptionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = mem_123; // string | The customer subscription ID

try {
    $result = $apiInstance->subscriptionsGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubscriptionsApi->subscriptionsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The customer subscription ID | |

### Return type

[**\Solifyn\Model\SubscriptionDetail**](../Model/SubscriptionDetail.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `subscriptionsList()`

```php
subscriptionsList($customer_id): \Solifyn\Model\SubscriptionList
```

List Subscriptions

Retrieve a list of customer subscriptions, optionally filtered by customer ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\SubscriptionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$customer_id = 'customer_id_example'; // string | Filter subscriptions by customer ID.

try {
    $result = $apiInstance->subscriptionsList($customer_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubscriptionsApi->subscriptionsList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **customer_id** | **string**| Filter subscriptions by customer ID. | [optional] |

### Return type

[**\Solifyn\Model\SubscriptionList**](../Model/SubscriptionList.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
