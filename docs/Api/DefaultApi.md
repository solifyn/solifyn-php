# Solifyn\DefaultApi

All URIs are relative to http://localhost:8000, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**disputeCreatedPost()**](DefaultApi.md#disputeCreatedPost) | **POST** /dispute.created | Dispute Created |
| [**disputeLostPost()**](DefaultApi.md#disputeLostPost) | **POST** /dispute.lost | Dispute Lost |
| [**disputeWonPost()**](DefaultApi.md#disputeWonPost) | **POST** /dispute.won | Dispute Won |
| [**licenseCreatedPost()**](DefaultApi.md#licenseCreatedPost) | **POST** /license.created | License Created |
| [**licenseRevokedPost()**](DefaultApi.md#licenseRevokedPost) | **POST** /license.revoked | License Revoked |
| [**paymentCreatedPost()**](DefaultApi.md#paymentCreatedPost) | **POST** /payment.created | Payment Created |
| [**paymentFailedPost()**](DefaultApi.md#paymentFailedPost) | **POST** /payment.failed | Payment Failed |
| [**paymentSucceededPost()**](DefaultApi.md#paymentSucceededPost) | **POST** /payment.succeeded | Payment Succeeded |
| [**refundFailedPost()**](DefaultApi.md#refundFailedPost) | **POST** /refund.failed | Refund Failed |
| [**refundSucceededPost()**](DefaultApi.md#refundSucceededPost) | **POST** /refund.succeeded | Refund Succeeded |
| [**subscriptionCreatedPost()**](DefaultApi.md#subscriptionCreatedPost) | **POST** /subscription.created | Subscription Created |
| [**subscriptionDeactivatedPost()**](DefaultApi.md#subscriptionDeactivatedPost) | **POST** /subscription.deactivated | Subscription Deactivated |
| [**subscriptionUpdatedPost()**](DefaultApi.md#subscriptionUpdatedPost) | **POST** /subscription.updated | Subscription Updated |


## `disputeCreatedPost()`

```php
disputeCreatedPost($webhook_dispute_payload)
```

Dispute Created

Occurs when a payment charge is disputed by the customer (chargeback initiated).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$webhook_dispute_payload = new \Solifyn\Model\WebhookDisputePayload(); // \Solifyn\Model\WebhookDisputePayload

try {
    $apiInstance->disputeCreatedPost($webhook_dispute_payload);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->disputeCreatedPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **webhook_dispute_payload** | [**\Solifyn\Model\WebhookDisputePayload**](../Model/WebhookDisputePayload.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `disputeLostPost()`

```php
disputeLostPost($webhook_dispute_payload)
```

Dispute Lost

Occurs when a dispute challenge is lost and the funds are returned to the cardholder.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$webhook_dispute_payload = new \Solifyn\Model\WebhookDisputePayload(); // \Solifyn\Model\WebhookDisputePayload

try {
    $apiInstance->disputeLostPost($webhook_dispute_payload);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->disputeLostPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **webhook_dispute_payload** | [**\Solifyn\Model\WebhookDisputePayload**](../Model/WebhookDisputePayload.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `disputeWonPost()`

```php
disputeWonPost($webhook_dispute_payload)
```

Dispute Won

Occurs when a dispute challenge is won by the merchant.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$webhook_dispute_payload = new \Solifyn\Model\WebhookDisputePayload(); // \Solifyn\Model\WebhookDisputePayload

try {
    $apiInstance->disputeWonPost($webhook_dispute_payload);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->disputeWonPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **webhook_dispute_payload** | [**\Solifyn\Model\WebhookDisputePayload**](../Model/WebhookDisputePayload.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `licenseCreatedPost()`

```php
licenseCreatedPost($webhook_license_payload)
```

License Created

Occurs when a new software license key is created or assigned to a customer purchase.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$webhook_license_payload = new \Solifyn\Model\WebhookLicensePayload(); // \Solifyn\Model\WebhookLicensePayload

try {
    $apiInstance->licenseCreatedPost($webhook_license_payload);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->licenseCreatedPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **webhook_license_payload** | [**\Solifyn\Model\WebhookLicensePayload**](../Model/WebhookLicensePayload.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `licenseRevokedPost()`

```php
licenseRevokedPost($webhook_license_payload)
```

License Revoked

Occurs when a software license key is revoked (e.g., due to subscription cancellation, refund, or dispute).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$webhook_license_payload = new \Solifyn\Model\WebhookLicensePayload(); // \Solifyn\Model\WebhookLicensePayload

try {
    $apiInstance->licenseRevokedPost($webhook_license_payload);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->licenseRevokedPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **webhook_license_payload** | [**\Solifyn\Model\WebhookLicensePayload**](../Model/WebhookLicensePayload.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `paymentCreatedPost()`

```php
paymentCreatedPost($webhook_payment_payload)
```

Payment Created

Occurs when a new payment is initiated (e.g., at checkout start or subscription creation). The payment may still be in an incomplete or pending state.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$webhook_payment_payload = {"id":"pay_123","status":"created","substatus":"incomplete","customerId":"usr_123","customerEmail":"customer@example.com","customerName":"John Doe","customerUsername":"johndoe","productTitle":"SaaS Pro Access","productRoute":"saas-pro-access","planId":"plan_123","membershipId":"mem_123","membershipStatus":"drafted","billingReason":"subscription_create","amount":"29.00","subtotal":"29.00","usdTotal":"29.00","feeAmount":"1.50","amountAfterFees":"27.50","taxAmount":null,"taxBehavior":null,"taxRefundedAmount":null,"refundedAmount":"0","settlementAmount":"29.00","settlementCurrency":"usd","settlementExchangeRate":null,"currency":"USD","refundable":false,"retryable":false,"autoRefunded":false,"paymentMethod":null,"cardBrand":null,"cardLast4":null,"cardExpMonth":null,"cardExpYear":null,"billingAddress":{"name":"John Doe","line1":"123 Main St","line2":"","city":"San Francisco","state":"CA","country":"US","postal_code":"94105"},"licenseKey":null,"filesSnapshot":null,"checkoutId":null,"discountCode":null,"failureMessage":null,"paidAt":"2026-05-25T20:20:05.000Z","refundedAt":null,"disputeAlertedAt":null,"lastPaymentAttempt":null,"nextPaymentAttempt":"2026-05-25T20:20:05.000Z","createdAt":"2026-05-25T20:20:06.000Z","updatedAt":"2026-05-25T20:20:06.000Z","paymentEventType":"payment.created","lastEventType":"payment.created","businessId":"biz_123"}; // \Solifyn\Model\WebhookPaymentPayload

try {
    $apiInstance->paymentCreatedPost($webhook_payment_payload);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->paymentCreatedPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **webhook_payment_payload** | [**\Solifyn\Model\WebhookPaymentPayload**](../Model/WebhookPaymentPayload.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `paymentFailedPost()`

```php
paymentFailedPost($order)
```

Payment Failed

Occurs when a customer payment attempt fails.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order = new \Solifyn\Model\Order(); // \Solifyn\Model\Order

try {
    $apiInstance->paymentFailedPost($order);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->paymentFailedPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order** | [**\Solifyn\Model\Order**](../Model/Order.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `paymentSucceededPost()`

```php
paymentSucceededPost($order)
```

Payment Succeeded

Occurs when a customer payment is confirmed as succeeded.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order = new \Solifyn\Model\Order(); // \Solifyn\Model\Order

try {
    $apiInstance->paymentSucceededPost($order);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->paymentSucceededPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order** | [**\Solifyn\Model\Order**](../Model/Order.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `refundFailedPost()`

```php
refundFailedPost($webhook_refund_payload)
```

Refund Failed

Occurs when a payment refund fails.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$webhook_refund_payload = new \Solifyn\Model\WebhookRefundPayload(); // \Solifyn\Model\WebhookRefundPayload

try {
    $apiInstance->refundFailedPost($webhook_refund_payload);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->refundFailedPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **webhook_refund_payload** | [**\Solifyn\Model\WebhookRefundPayload**](../Model/WebhookRefundPayload.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `refundSucceededPost()`

```php
refundSucceededPost($webhook_refund_payload)
```

Refund Succeeded

Occurs when a payment refund is confirmed as succeeded.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$webhook_refund_payload = new \Solifyn\Model\WebhookRefundPayload(); // \Solifyn\Model\WebhookRefundPayload

try {
    $apiInstance->refundSucceededPost($webhook_refund_payload);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->refundSucceededPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **webhook_refund_payload** | [**\Solifyn\Model\WebhookRefundPayload**](../Model/WebhookRefundPayload.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `subscriptionCreatedPost()`

```php
subscriptionCreatedPost($webhook_subscription_payload)
```

Subscription Created

Occurs when a customer subscription is successfully started.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$webhook_subscription_payload = new \Solifyn\Model\WebhookSubscriptionPayload(); // \Solifyn\Model\WebhookSubscriptionPayload

try {
    $apiInstance->subscriptionCreatedPost($webhook_subscription_payload);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->subscriptionCreatedPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **webhook_subscription_payload** | [**\Solifyn\Model\WebhookSubscriptionPayload**](../Model/WebhookSubscriptionPayload.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `subscriptionDeactivatedPost()`

```php
subscriptionDeactivatedPost($webhook_subscription_payload)
```

Subscription Deactivated

Occurs when a customer subscription is deactivated or expired.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$webhook_subscription_payload = new \Solifyn\Model\WebhookSubscriptionPayload(); // \Solifyn\Model\WebhookSubscriptionPayload

try {
    $apiInstance->subscriptionDeactivatedPost($webhook_subscription_payload);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->subscriptionDeactivatedPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **webhook_subscription_payload** | [**\Solifyn\Model\WebhookSubscriptionPayload**](../Model/WebhookSubscriptionPayload.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `subscriptionUpdatedPost()`

```php
subscriptionUpdatedPost($webhook_subscription_payload)
```

Subscription Updated

Occurs when a customer subscription is updated (e.g., cancel at period end changes).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Key) authorization: ApiKeyAuth
$config = Solifyn\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Solifyn\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$webhook_subscription_payload = new \Solifyn\Model\WebhookSubscriptionPayload(); // \Solifyn\Model\WebhookSubscriptionPayload

try {
    $apiInstance->subscriptionUpdatedPost($webhook_subscription_payload);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->subscriptionUpdatedPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **webhook_subscription_payload** | [**\Solifyn\Model\WebhookSubscriptionPayload**](../Model/WebhookSubscriptionPayload.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
