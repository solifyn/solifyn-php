# solifyn

Welcome to the Solifyn API Reference. Leverage our secure endpoints to manage products and issue, validate, and manage software license keys programmatically.


## Installation & Usage

### Requirements

PHP 7.4 and later.
Should also work with PHP 8.0.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/solifyn/solifyn-php.git"
    }
  ],
  "require": {
    "solifyn/solifyn-php": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/solifyn/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');




$apiInstance = new Solifyn\Api\BalanceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $apiInstance->balanceControllerFindAll();
} catch (Exception $e) {
    echo 'Exception when calling BalanceApi->balanceControllerFindAll: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *https://api.solifyn.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*BalanceApi* | [**balanceControllerFindAll**](docs/Api/BalanceApi.md#balancecontrollerfindall) | **GET** /v1/balances | 
*BalanceApi* | [**balanceControllerGenerateReport**](docs/Api/BalanceApi.md#balancecontrollergeneratereport) | **GET** /v1/balances/report | 
*BalanceApi* | [**balanceControllerGetSummary**](docs/Api/BalanceApi.md#balancecontrollergetsummary) | **GET** /v1/balances/summary | 
*CheckoutApi* | [**checkoutCreate**](docs/Api/CheckoutApi.md#checkoutcreate) | **POST** /v1/checkout/create | Create Checkout Session
*CheckoutApi* | [**checkoutCreateCollection**](docs/Api/CheckoutApi.md#checkoutcreatecollection) | **POST** /v1/checkout/collection/create | Create Collection Checkout Session
*CheckoutApi* | [**checkoutCreateSetup**](docs/Api/CheckoutApi.md#checkoutcreatesetup) | **POST** /v1/checkout/setup-configuration | Create Setup Checkout Configuration
*CheckoutApi* | [**checkoutGetSession**](docs/Api/CheckoutApi.md#checkoutgetsession) | **GET** /v1/checkout/session/{id} | Get Checkout Session Details
*CheckoutApi* | [**checkoutPricePreview**](docs/Api/CheckoutApi.md#checkoutpricepreview) | **GET** /v1/checkout/price-preview | Get Converted Price Preview
*CheckoutApi* | [**checkoutSupportedCurrencies**](docs/Api/CheckoutApi.md#checkoutsupportedcurrencies) | **GET** /v1/checkout/supported-currencies | Get Supported Currencies
*CheckoutLinksApi* | [**checkoutLinksCreate**](docs/Api/CheckoutLinksApi.md#checkoutlinkscreate) | **POST** /v1/checkout-links | Create Checkout Link
*CheckoutLinksApi* | [**checkoutLinksDelete**](docs/Api/CheckoutLinksApi.md#checkoutlinksdelete) | **DELETE** /v1/checkout-links/{id} | Delete Checkout Link
*CheckoutLinksApi* | [**checkoutLinksGet**](docs/Api/CheckoutLinksApi.md#checkoutlinksget) | **GET** /v1/checkout-links/{id} | Retrieve Checkout Link Details
*CheckoutLinksApi* | [**checkoutLinksList**](docs/Api/CheckoutLinksApi.md#checkoutlinkslist) | **GET** /v1/checkout-links | List Checkout Links
*CheckoutLinksApi* | [**checkoutLinksUpdate**](docs/Api/CheckoutLinksApi.md#checkoutlinksupdate) | **PATCH** /v1/checkout-links/{id} | Update Checkout Link
*CollectionsApi* | [**collectionsAddProducts**](docs/Api/CollectionsApi.md#collectionsaddproducts) | **POST** /v1/collections/{id}/products | Add Products to Collection
*CollectionsApi* | [**collectionsArchive**](docs/Api/CollectionsApi.md#collectionsarchive) | **DELETE** /v1/collections/{id} | Archive Collection
*CollectionsApi* | [**collectionsCreate**](docs/Api/CollectionsApi.md#collectionscreate) | **POST** /v1/collections | Create Collection
*CollectionsApi* | [**collectionsDeleteProduct**](docs/Api/CollectionsApi.md#collectionsdeleteproduct) | **DELETE** /v1/collections/{id}/products/{productId} | Remove Product from Collection
*CollectionsApi* | [**collectionsGet**](docs/Api/CollectionsApi.md#collectionsget) | **GET** /v1/collections/{id} | Retrieve Collection
*CollectionsApi* | [**collectionsList**](docs/Api/CollectionsApi.md#collectionslist) | **GET** /v1/collections | List Collections
*CollectionsApi* | [**collectionsListArchived**](docs/Api/CollectionsApi.md#collectionslistarchived) | **GET** /v1/collections/archived | List Archived Collections
*CollectionsApi* | [**collectionsUnarchive**](docs/Api/CollectionsApi.md#collectionsunarchive) | **POST** /v1/collections/{id}/unarchive | Unarchive Collection
*CollectionsApi* | [**collectionsUpdate**](docs/Api/CollectionsApi.md#collectionsupdate) | **PATCH** /v1/collections/{id} | Update Collection
*CollectionsApi* | [**collectionsUpdateProduct**](docs/Api/CollectionsApi.md#collectionsupdateproduct) | **PATCH** /v1/collections/{id}/products/{productId} | Update Collection Product
*CustomersApi* | [**customersCreate**](docs/Api/CustomersApi.md#customerscreate) | **POST** /v1/customers | Create Customer
*CustomersApi* | [**customersGenerateInvite**](docs/Api/CustomersApi.md#customersgenerateinvite) | **POST** /v1/customers/{id}/share | Generate Shared Invite
*CustomersApi* | [**customersGet**](docs/Api/CustomersApi.md#customersget) | **GET** /v1/customers/{id} | Retrieve Customer
*CustomersApi* | [**customersList**](docs/Api/CustomersApi.md#customerslist) | **GET** /v1/customers | List Customers
*CustomersApi* | [**customersUpdate**](docs/Api/CustomersApi.md#customersupdate) | **PATCH** /v1/customers/{id} | Update Customer
*DeveloperApi* | [**developerCreateApiKey**](docs/Api/DeveloperApi.md#developercreateapikey) | **POST** /v1/developer/api-keys | Create Developer API Key
*DeveloperApi* | [**developerCreateWebhook**](docs/Api/DeveloperApi.md#developercreatewebhook) | **POST** /v1/developer/webhooks | Create Webhook Endpoint
*DeveloperApi* | [**developerDeleteWebhook**](docs/Api/DeveloperApi.md#developerdeletewebhook) | **DELETE** /v1/developer/webhooks/{id} | Delete Webhook Endpoint
*DeveloperApi* | [**developerGetAppPortal**](docs/Api/DeveloperApi.md#developergetappportal) | **GET** /v1/developer/webhooks/app-portal | Retrieve Hosted Webhooks Portal URL
*DeveloperApi* | [**developerGetWebhook**](docs/Api/DeveloperApi.md#developergetwebhook) | **GET** /v1/developer/webhooks/{id} | Retrieve Webhook Endpoint Details
*DeveloperApi* | [**developerListApiKeys**](docs/Api/DeveloperApi.md#developerlistapikeys) | **GET** /v1/developer/api-keys | List Developer API Keys
*DeveloperApi* | [**developerListWebhookDeliveries**](docs/Api/DeveloperApi.md#developerlistwebhookdeliveries) | **GET** /v1/developer/webhooks/{id}/deliveries | Retrieve Webhook Delivery Logs
*DeveloperApi* | [**developerListWebhooks**](docs/Api/DeveloperApi.md#developerlistwebhooks) | **GET** /v1/developer/webhooks | List Webhook Endpoints
*DeveloperApi* | [**developerRevokeApiKey**](docs/Api/DeveloperApi.md#developerrevokeapikey) | **DELETE** /v1/developer/api-keys/{id} | Revoke API Key
*DeveloperApi* | [**developerUpdateWebhook**](docs/Api/DeveloperApi.md#developerupdatewebhook) | **PATCH** /v1/developer/webhooks/{id} | Update Webhook Endpoint
*DigitalFileApi* | [**digitalFileControllerCreate**](docs/Api/DigitalFileApi.md#digitalfilecontrollercreate) | **POST** /v1/digital-files | 
*DigitalFileApi* | [**digitalFileControllerFindAll**](docs/Api/DigitalFileApi.md#digitalfilecontrollerfindall) | **GET** /v1/digital-files | 
*DigitalFileApi* | [**digitalFileControllerRemove**](docs/Api/DigitalFileApi.md#digitalfilecontrollerremove) | **DELETE** /v1/digital-files/{id} | 
*DiscordIntegrationApi* | [**discordGetInstallUrl**](docs/Api/DiscordIntegrationApi.md#discordgetinstallurl) | **GET** /v1/discord/install | Get Discord Bot Installation URL
*DiscordIntegrationApi* | [**discordListRoles**](docs/Api/DiscordIntegrationApi.md#discordlistroles) | **GET** /v1/discord/roles | List Guild Discord Roles
*DiscountsApi* | [**discountsCreate**](docs/Api/DiscountsApi.md#discountscreate) | **POST** /v1/discounts | Create Discount
*DiscountsApi* | [**discountsDelete**](docs/Api/DiscountsApi.md#discountsdelete) | **DELETE** /v1/discounts/{id} | Delete Discount
*DiscountsApi* | [**discountsGet**](docs/Api/DiscountsApi.md#discountsget) | **GET** /v1/discounts/{id} | Retrieve Discount
*DiscountsApi* | [**discountsList**](docs/Api/DiscountsApi.md#discountslist) | **GET** /v1/discounts | List Discounts
*DiscountsApi* | [**discountsUpdate**](docs/Api/DiscountsApi.md#discountsupdate) | **PATCH** /v1/discounts/{id} | Update Discount
*DiscountsApi* | [**discountsValidate**](docs/Api/DiscountsApi.md#discountsvalidate) | **GET** /v1/discounts/validate | Validate Code
*DisputesApi* | [**disputesGenerateReport**](docs/Api/DisputesApi.md#disputesgeneratereport) | **GET** /v1/transactions/disputes/report | Generate Dispute CSV Report
*DisputesApi* | [**disputesGet**](docs/Api/DisputesApi.md#disputesget) | **GET** /v1/transactions/disputes/{id} | Retrieve Dispute
*DisputesApi* | [**disputesList**](docs/Api/DisputesApi.md#disputeslist) | **GET** /v1/transactions/disputes | List Disputes
*DisputesApi* | [**disputesSubmitEvidence**](docs/Api/DisputesApi.md#disputessubmitevidence) | **POST** /v1/transactions/disputes/{id}/submit | Submit Dispute Evidence
*DisputesApi* | [**disputesUpdateEvidence**](docs/Api/DisputesApi.md#disputesupdateevidence) | **PATCH** /v1/transactions/disputes/{id}/evidence | Update Dispute Evidence
*DisputesApi* | [**disputesUploadEvidenceFile**](docs/Api/DisputesApi.md#disputesuploadevidencefile) | **POST** /v1/transactions/disputes/upload | Upload Evidence File
*EntitlementGrantsApi* | [**entitlementGrantsGet**](docs/Api/EntitlementGrantsApi.md#entitlementgrantsget) | **GET** /v1/entitlement-grants/{id} | Retrieve Entitlement Grant
*EntitlementGrantsApi* | [**entitlementGrantsList**](docs/Api/EntitlementGrantsApi.md#entitlementgrantslist) | **GET** /v1/entitlement-grants | List Entitlement Grants
*EntitlementGrantsApi* | [**entitlementGrantsRetry**](docs/Api/EntitlementGrantsApi.md#entitlementgrantsretry) | **POST** /v1/entitlement-grants/{id}/retry | Retry Entitlement Grant Delivery
*EntitlementGrantsApi* | [**entitlementGrantsRevoke**](docs/Api/EntitlementGrantsApi.md#entitlementgrantsrevoke) | **POST** /v1/entitlement-grants/{id}/revoke | Manually Revoke Entitlement Grant
*GitHubIntegrationApi* | [**githubGetInstallUrl**](docs/Api/GitHubIntegrationApi.md#githubgetinstallurl) | **GET** /v1/github/install | Get GitHub App Installation URL
*GitHubIntegrationApi* | [**githubListRepos**](docs/Api/GitHubIntegrationApi.md#githublistrepos) | **GET** /v1/github/repos | List Available GitHub Repositories
*LicenseApi* | [**licensesCreate**](docs/Api/LicenseApi.md#licensescreate) | **POST** /v1/licenses | Create License Key
*LicenseApi* | [**licensesDeleteInstance**](docs/Api/LicenseApi.md#licensesdeleteinstance) | **DELETE** /v1/licenses/instances/{instanceId} | Force Delete Instance
*LicenseApi* | [**licensesGet**](docs/Api/LicenseApi.md#licensesget) | **GET** /v1/licenses/{id} | Get License Key
*LicenseApi* | [**licensesGetInstance**](docs/Api/LicenseApi.md#licensesgetinstance) | **GET** /v1/licenses/{id}/instances/{instanceId} | Get License Key Instance
*LicenseApi* | [**licensesGetInstances**](docs/Api/LicenseApi.md#licensesgetinstances) | **GET** /v1/licenses/{id}/instances | Get License Key Instances
*LicenseApi* | [**licensesList**](docs/Api/LicenseApi.md#licenseslist) | **GET** /v1/licenses | List License Keys
*LicenseApi* | [**licensesToggle**](docs/Api/LicenseApi.md#licensestoggle) | **POST** /v1/licenses/{id}/toggle | Toggle License Status
*LicenseApi* | [**licensesUpdate**](docs/Api/LicenseApi.md#licensesupdate) | **PATCH** /v1/licenses/{id} | Update License Key
*LicenseApi* | [**licensesUpdateInstance**](docs/Api/LicenseApi.md#licensesupdateinstance) | **PATCH** /v1/licenses/{id}/instances/{instanceId} | Update License Key Instance
*LicenseApi* | [**licensesUpdateInstancePost**](docs/Api/LicenseApi.md#licensesupdateinstancepost) | **POST** /v1/licenses/{id}/instances/{instanceId} | Update License Key Instance (POST)
*LicenseKeysApi* | [**licensesCreate**](docs/Api/LicenseKeysApi.md#licensescreate) | **POST** /v1/licenses | Create License Key
*LicenseKeysApi* | [**licensesDeleteInstance**](docs/Api/LicenseKeysApi.md#licensesdeleteinstance) | **DELETE** /v1/licenses/instances/{instanceId} | Force Delete Instance
*LicenseKeysApi* | [**licensesGet**](docs/Api/LicenseKeysApi.md#licensesget) | **GET** /v1/licenses/{id} | Get License Key
*LicenseKeysApi* | [**licensesGetInstance**](docs/Api/LicenseKeysApi.md#licensesgetinstance) | **GET** /v1/licenses/{id}/instances/{instanceId} | Get License Key Instance
*LicenseKeysApi* | [**licensesGetInstances**](docs/Api/LicenseKeysApi.md#licensesgetinstances) | **GET** /v1/licenses/{id}/instances | Get License Key Instances
*LicenseKeysApi* | [**licensesList**](docs/Api/LicenseKeysApi.md#licenseslist) | **GET** /v1/licenses | List License Keys
*LicenseKeysApi* | [**licensesToggle**](docs/Api/LicenseKeysApi.md#licensestoggle) | **POST** /v1/licenses/{id}/toggle | Toggle License Status
*LicenseKeysApi* | [**licensesUpdate**](docs/Api/LicenseKeysApi.md#licensesupdate) | **PATCH** /v1/licenses/{id} | Update License Key
*LicenseKeysApi* | [**licensesUpdateInstance**](docs/Api/LicenseKeysApi.md#licensesupdateinstance) | **PATCH** /v1/licenses/{id}/instances/{instanceId} | Update License Key Instance
*LicenseKeysApi* | [**licensesUpdateInstancePost**](docs/Api/LicenseKeysApi.md#licensesupdateinstancepost) | **POST** /v1/licenses/{id}/instances/{instanceId} | Update License Key Instance (POST)
*LicenseKeysClientApi* | [**licensesActivate**](docs/Api/LicenseKeysClientApi.md#licensesactivate) | **POST** /v1/licenses/activate | Activate License Key
*LicenseKeysClientApi* | [**licensesDeactivate**](docs/Api/LicenseKeysClientApi.md#licensesdeactivate) | **POST** /v1/licenses/deactivate/{instanceId} | Deactivate Instance
*LicenseKeysClientApi* | [**licensesInstances**](docs/Api/LicenseKeysClientApi.md#licensesinstances) | **GET** /v1/licenses/instances/{licenseId} | Get Active Instances
*LicenseKeysClientApi* | [**licensesVerify**](docs/Api/LicenseKeysClientApi.md#licensesverify) | **POST** /v1/licenses/verify | Validate License Key
*MetersApi* | [**eventsIngest**](docs/Api/MetersApi.md#eventsingest) | **POST** /v1/meters/ingest | Ingest Events
*MetersApi* | [**metersCreate**](docs/Api/MetersApi.md#meterscreate) | **POST** /v1/meters | Create Meter
*MetersApi* | [**metersGet**](docs/Api/MetersApi.md#metersget) | **GET** /v1/meters/{id} | Retrieve Meter
*MetersApi* | [**metersGetEvents**](docs/Api/MetersApi.md#metersgetevents) | **GET** /v1/meters/{id}/events | List Meter Events
*MetersApi* | [**metersGetQuantities**](docs/Api/MetersApi.md#metersgetquantities) | **GET** /v1/meters/{id}/quantities | Get Meter Quantities
*MetersApi* | [**metersList**](docs/Api/MetersApi.md#meterslist) | **GET** /v1/meters | List Meters
*MetersApi* | [**metersUpdate**](docs/Api/MetersApi.md#metersupdate) | **PATCH** /v1/meters/{id} | Update Meter
*OrdersApi* | [**ordersGet**](docs/Api/OrdersApi.md#ordersget) | **GET** /v1/orders/{id} | Retrieve Order
*OrdersApi* | [**ordersGetInvoice**](docs/Api/OrdersApi.md#ordersgetinvoice) | **GET** /v1/orders/{id}/invoice | Get Order Invoice
*OrdersApi* | [**ordersList**](docs/Api/OrdersApi.md#orderslist) | **GET** /v1/orders | List Orders
*OrdersApi* | [**ordersUpdate**](docs/Api/OrdersApi.md#ordersupdate) | **PATCH** /v1/orders/{id} | Update Order Billing Address
*OrdersApi* | [**refundsCreate**](docs/Api/OrdersApi.md#refundscreate) | **POST** /v1/orders/{id}/refund | Create Refund
*ProductAddOnsApi* | [**productsCreateAddon**](docs/Api/ProductAddOnsApi.md#productscreateaddon) | **POST** /v1/products/{id}/addons | Create Product Add-on
*ProductAddOnsApi* | [**productsDeleteAddon**](docs/Api/ProductAddOnsApi.md#productsdeleteaddon) | **DELETE** /v1/products/{id}/addons/{addonId} | Delete Product Add-on
*ProductAddOnsApi* | [**productsGetAddon**](docs/Api/ProductAddOnsApi.md#productsgetaddon) | **GET** /v1/products/{id}/addons/{addonId} | Retrieve Product Add-on
*ProductAddOnsApi* | [**productsListAddons**](docs/Api/ProductAddOnsApi.md#productslistaddons) | **GET** /v1/products/{id}/addons | List Product Add-ons
*ProductAddOnsApi* | [**productsListAllAddons**](docs/Api/ProductAddOnsApi.md#productslistalladdons) | **GET** /v1/products/all-addons/list | List All Add-ons
*ProductAddOnsApi* | [**productsUpdateAddon**](docs/Api/ProductAddOnsApi.md#productsupdateaddon) | **PATCH** /v1/products/{id}/addons/{addonId} | Update Product Add-on
*ProductsApi* | [**productsArchive**](docs/Api/ProductsApi.md#productsarchive) | **DELETE** /v1/products/{id} | Archive Product
*ProductsApi* | [**productsCreate**](docs/Api/ProductsApi.md#productscreate) | **POST** /v1/products | Create Product
*ProductsApi* | [**productsGet**](docs/Api/ProductsApi.md#productsget) | **GET** /v1/products/{id} | Retrieve Product
*ProductsApi* | [**productsList**](docs/Api/ProductsApi.md#productslist) | **GET** /v1/products | List Products
*ProductsApi* | [**productsUnarchive**](docs/Api/ProductsApi.md#productsunarchive) | **POST** /v1/products/{id}/unarchive | Unarchive Product
*ProductsApi* | [**productsUpdate**](docs/Api/ProductsApi.md#productsupdate) | **PATCH** /v1/products/{id} | Update Product
*RefundRequestsApi* | [**refundRequestsList**](docs/Api/RefundRequestsApi.md#refundrequestslist) | **GET** /v1/refund-requests | List Refund Requests (Merchant)
*RefundRequestsApi* | [**refundRequestsListMessages**](docs/Api/RefundRequestsApi.md#refundrequestslistmessages) | **GET** /v1/refund-requests/{id}/messages | List Messages for Refund Request (Merchant)
*RefundRequestsApi* | [**refundRequestsSendMessage**](docs/Api/RefundRequestsApi.md#refundrequestssendmessage) | **POST** /v1/refund-requests/{id}/messages | Send Refund Request Message (Merchant)
*RefundRequestsApi* | [**refundRequestsUpdateStatus**](docs/Api/RefundRequestsApi.md#refundrequestsupdatestatus) | **PATCH** /v1/refund-requests/{id}/status | Update Refund Request Status (Merchant)
*RefundRequestsApi* | [**refundRequestsUploadEvidence**](docs/Api/RefundRequestsApi.md#refundrequestsuploadevidence) | **POST** /v1/refund-requests/upload-evidence | Upload Dispute Evidence File (Merchant)
*RefundsChargebacksApi* | [**refundsCreate**](docs/Api/RefundsChargebacksApi.md#refundscreate) | **POST** /v1/orders/{id}/refund | Create Refund
*RefundsChargebacksApi* | [**refundsGet**](docs/Api/RefundsChargebacksApi.md#refundsget) | **GET** /v1/refunds/{id} | Retrieve Refund details
*RefundsChargebacksApi* | [**refundsList**](docs/Api/RefundsChargebacksApi.md#refundslist) | **GET** /v1/refunds | List Refunds
*SubscriptionsApi* | [**subscriptionsAction**](docs/Api/SubscriptionsApi.md#subscriptionsaction) | **POST** /v1/subscriptions/{subscriptionId}/{action} | Subscription Action
*SubscriptionsApi* | [**subscriptionsGet**](docs/Api/SubscriptionsApi.md#subscriptionsget) | **GET** /v1/subscriptions/{id} | Retrieve Subscription Details
*SubscriptionsApi* | [**subscriptionsList**](docs/Api/SubscriptionsApi.md#subscriptionslist) | **GET** /v1/subscriptions | List Subscriptions
*WebhookApi* | [**webhookControllerHandleSvixWebhook**](docs/Api/WebhookApi.md#webhookcontrollerhandlesvixwebhook) | **POST** /v1/webhook/svix | 
*WebhookApi* | [**webhookControllerHandleWebhook**](docs/Api/WebhookApi.md#webhookcontrollerhandlewebhook) | **POST** /v1/webhook | 
*WebhookEndpointApi* | [**operationalWebhookControllerCreate**](docs/Api/WebhookEndpointApi.md#operationalwebhookcontrollercreate) | **POST** /v1/operational-webhook/endpoint | Create Operational Webhook Endpoint
*WebhookEndpointApi* | [**operationalWebhookControllerDelete**](docs/Api/WebhookEndpointApi.md#operationalwebhookcontrollerdelete) | **DELETE** /v1/operational-webhook/endpoint/{id} | Delete Operational Webhook Endpoint
*WebhookEndpointApi* | [**operationalWebhookControllerGet**](docs/Api/WebhookEndpointApi.md#operationalwebhookcontrollerget) | **GET** /v1/operational-webhook/endpoint/{id} | Get Operational Webhook Endpoint
*WebhookEndpointApi* | [**operationalWebhookControllerGetHeaders**](docs/Api/WebhookEndpointApi.md#operationalwebhookcontrollergetheaders) | **GET** /v1/operational-webhook/endpoint/{id}/headers | Get Operational Webhook Endpoint Headers
*WebhookEndpointApi* | [**operationalWebhookControllerGetSecret**](docs/Api/WebhookEndpointApi.md#operationalwebhookcontrollergetsecret) | **GET** /v1/operational-webhook/endpoint/{id}/secret | Get Operational Webhook Endpoint Secret
*WebhookEndpointApi* | [**operationalWebhookControllerList**](docs/Api/WebhookEndpointApi.md#operationalwebhookcontrollerlist) | **GET** /v1/operational-webhook/endpoint | List Operational Webhook Endpoints
*WebhookEndpointApi* | [**operationalWebhookControllerRotateSecret**](docs/Api/WebhookEndpointApi.md#operationalwebhookcontrollerrotatesecret) | **POST** /v1/operational-webhook/endpoint/{id}/secret/rotate | Rotate Operational Webhook Endpoint Secret
*WebhookEndpointApi* | [**operationalWebhookControllerUpdate**](docs/Api/WebhookEndpointApi.md#operationalwebhookcontrollerupdate) | **PUT** /v1/operational-webhook/endpoint/{id} | Update Operational Webhook Endpoint
*WebhookEndpointApi* | [**operationalWebhookControllerUpdateHeaders**](docs/Api/WebhookEndpointApi.md#operationalwebhookcontrollerupdateheaders) | **PUT** /v1/operational-webhook/endpoint/{id}/headers | Set Operational Webhook Endpoint Headers

## Models

- [AddCollectionProductsDto](docs/Model/AddCollectionProductsDto.md)
- [Addon](docs/Model/Addon.md)
- [AddonCreate](docs/Model/AddonCreate.md)
- [AddonUpdate](docs/Model/AddonUpdate.md)
- [ApiKeyResponseDto](docs/Model/ApiKeyResponseDto.md)
- [AppPortalUrlResponseDto](docs/Model/AppPortalUrlResponseDto.md)
- [Brand](docs/Model/Brand.md)
- [BrandCreate](docs/Model/BrandCreate.md)
- [BrandUpdate](docs/Model/BrandUpdate.md)
- [CheckoutLinkMessageResponseDto](docs/Model/CheckoutLinkMessageResponseDto.md)
- [CheckoutLinkResponseDto](docs/Model/CheckoutLinkResponseDto.md)
- [CheckoutResponseDto](docs/Model/CheckoutResponseDto.md)
- [CheckoutSessionDetailsDto](docs/Model/CheckoutSessionDetailsDto.md)
- [CollectionArchivedResponseDto](docs/Model/CollectionArchivedResponseDto.md)
- [CollectionDetailResponseDto](docs/Model/CollectionDetailResponseDto.md)
- [CollectionProductDeletedResponseDto](docs/Model/CollectionProductDeletedResponseDto.md)
- [CollectionProductDto](docs/Model/CollectionProductDto.md)
- [CollectionProductEntry](docs/Model/CollectionProductEntry.md)
- [CollectionProductRefDto](docs/Model/CollectionProductRefDto.md)
- [CollectionProductUpdatedResponseDto](docs/Model/CollectionProductUpdatedResponseDto.md)
- [CollectionResponseDto](docs/Model/CollectionResponseDto.md)
- [CollectionUnarchivedResponseDto](docs/Model/CollectionUnarchivedResponseDto.md)
- [CollectionUpdatedResponseDto](docs/Model/CollectionUpdatedResponseDto.md)
- [CreateApiKeyDto](docs/Model/CreateApiKeyDto.md)
- [CreateCheckoutDto](docs/Model/CreateCheckoutDto.md)
- [CreateCheckoutLinkDto](docs/Model/CreateCheckoutLinkDto.md)
- [CreateCollectionCheckoutDto](docs/Model/CreateCollectionCheckoutDto.md)
- [CreateCollectionDto](docs/Model/CreateCollectionDto.md)
- [CreateCustomerDto](docs/Model/CreateCustomerDto.md)
- [CreateMeterDto](docs/Model/CreateMeterDto.md)
- [CreateSetupCheckoutDto](docs/Model/CreateSetupCheckoutDto.md)
- [CreateWebhookEndpointDto](docs/Model/CreateWebhookEndpointDto.md)
- [CustomerListResponseDto](docs/Model/CustomerListResponseDto.md)
- [CustomerMessageResponseDto](docs/Model/CustomerMessageResponseDto.md)
- [CustomerResponseDto](docs/Model/CustomerResponseDto.md)
- [CustomerSharedInviteResponseDto](docs/Model/CustomerSharedInviteResponseDto.md)
- [DashboardStatsDto](docs/Model/DashboardStatsDto.md)
- [DiscordRolesResponseDto](docs/Model/DiscordRolesResponseDto.md)
- [Discount](docs/Model/Discount.md)
- [DiscountCreate](docs/Model/DiscountCreate.md)
- [DiscountUpdate](docs/Model/DiscountUpdate.md)
- [DiscountsList200Response](docs/Model/DiscountsList200Response.md)
- [DiscountsList200ResponsePagination](docs/Model/DiscountsList200ResponsePagination.md)
- [Dispute](docs/Model/Dispute.md)
- [DisputeAttachmentDto](docs/Model/DisputeAttachmentDto.md)
- [DisputeEvidenceDto](docs/Model/DisputeEvidenceDto.md)
- [DisputeEvidenceUpdate](docs/Model/DisputeEvidenceUpdate.md)
- [DisputeFileUpload](docs/Model/DisputeFileUpload.md)
- [DisputeList](docs/Model/DisputeList.md)
- [DisputeListMetaDto](docs/Model/DisputeListMetaDto.md)
- [EntitlementGrantResponseDto](docs/Model/EntitlementGrantResponseDto.md)
- [GithubReposResponseDto](docs/Model/GithubReposResponseDto.md)
- [Instance](docs/Model/Instance.md)
- [Invoice](docs/Model/Invoice.md)
- [License](docs/Model/License.md)
- [LicenseSubDto](docs/Model/LicenseSubDto.md)
- [LicenseValidationResponse](docs/Model/LicenseValidationResponse.md)
- [LicensesActivateRequest](docs/Model/LicensesActivateRequest.md)
- [LicensesCreateRequest](docs/Model/LicensesCreateRequest.md)
- [LicensesDeactivate200Response](docs/Model/LicensesDeactivate200Response.md)
- [LicensesDeactivateRequest](docs/Model/LicensesDeactivateRequest.md)
- [LicensesUpdateInstancePostRequest](docs/Model/LicensesUpdateInstancePostRequest.md)
- [LicensesUpdateRequest](docs/Model/LicensesUpdateRequest.md)
- [LicensesVerifyRequest](docs/Model/LicensesVerifyRequest.md)
- [MeterDetailResponseDto](docs/Model/MeterDetailResponseDto.md)
- [MeterEventsResponseDto](docs/Model/MeterEventsResponseDto.md)
- [MeterIngestEventDto](docs/Model/MeterIngestEventDto.md)
- [MeterIngestRequestDto](docs/Model/MeterIngestRequestDto.md)
- [MeterIngestResponseDto](docs/Model/MeterIngestResponseDto.md)
- [MeterQuantitiesCostDto](docs/Model/MeterQuantitiesCostDto.md)
- [MeterQuantitiesResponseDto](docs/Model/MeterQuantitiesResponseDto.md)
- [MeterResponseDto](docs/Model/MeterResponseDto.md)
- [MeterUsageEventDto](docs/Model/MeterUsageEventDto.md)
- [OperationalWebhookEndpointHeadersInDto](docs/Model/OperationalWebhookEndpointHeadersInDto.md)
- [OperationalWebhookEndpointHeadersResponseDto](docs/Model/OperationalWebhookEndpointHeadersResponseDto.md)
- [OperationalWebhookEndpointInDto](docs/Model/OperationalWebhookEndpointInDto.md)
- [OperationalWebhookEndpointListResponseDto](docs/Model/OperationalWebhookEndpointListResponseDto.md)
- [OperationalWebhookEndpointResponseDto](docs/Model/OperationalWebhookEndpointResponseDto.md)
- [OperationalWebhookEndpointSecretInDto](docs/Model/OperationalWebhookEndpointSecretInDto.md)
- [OperationalWebhookEndpointSecretResponseDto](docs/Model/OperationalWebhookEndpointSecretResponseDto.md)
- [OperationalWebhookEndpointUpdateDto](docs/Model/OperationalWebhookEndpointUpdateDto.md)
- [Order](docs/Model/Order.md)
- [OrderBilling](docs/Model/OrderBilling.md)
- [OrderBillingUpdate](docs/Model/OrderBillingUpdate.md)
- [OrderCustomer](docs/Model/OrderCustomer.md)
- [OrderDetail](docs/Model/OrderDetail.md)
- [OrderList](docs/Model/OrderList.md)
- [OrderProductCart](docs/Model/OrderProductCart.md)
- [OrderRefund](docs/Model/OrderRefund.md)
- [OrderRefundCreate](docs/Model/OrderRefundCreate.md)
- [OrderUpdate](docs/Model/OrderUpdate.md)
- [PricePreviewResponseDto](docs/Model/PricePreviewResponseDto.md)
- [Product](docs/Model/Product.md)
- [ProductCreate](docs/Model/ProductCreate.md)
- [ProductCreateAddonsInner](docs/Model/ProductCreateAddonsInner.md)
- [ProductCreateCustomFieldsInner](docs/Model/ProductCreateCustomFieldsInner.md)
- [ProductMessageResponseDto](docs/Model/ProductMessageResponseDto.md)
- [ProductSubDto](docs/Model/ProductSubDto.md)
- [ProductUpdate](docs/Model/ProductUpdate.md)
- [ProductsArchive200Response](docs/Model/ProductsArchive200Response.md)
- [ProductsList200Response](docs/Model/ProductsList200Response.md)
- [ProductsList200ResponsePagination](docs/Model/ProductsList200ResponsePagination.md)
- [ProductsUnarchive200Response](docs/Model/ProductsUnarchive200Response.md)
- [Refund](docs/Model/Refund.md)
- [ResolvedAddon](docs/Model/ResolvedAddon.md)
- [RevokeSeatDto](docs/Model/RevokeSeatDto.md)
- [Subscription](docs/Model/Subscription.md)
- [SubscriptionAction](docs/Model/SubscriptionAction.md)
- [SubscriptionCompanyDto](docs/Model/SubscriptionCompanyDto.md)
- [SubscriptionDetail](docs/Model/SubscriptionDetail.md)
- [SubscriptionDetailProduct](docs/Model/SubscriptionDetailProduct.md)
- [SubscriptionList](docs/Model/SubscriptionList.md)
- [SubscriptionMemberDto](docs/Model/SubscriptionMemberDto.md)
- [SubscriptionPlanDto](docs/Model/SubscriptionPlanDto.md)
- [SubscriptionProductDto](docs/Model/SubscriptionProductDto.md)
- [SubscriptionSeatAdjustment](docs/Model/SubscriptionSeatAdjustment.md)
- [SubscriptionUserDto](docs/Model/SubscriptionUserDto.md)
- [SubscriptionsAction201Response](docs/Model/SubscriptionsAction201Response.md)
- [SupportedCurrenciesResponseDto](docs/Model/SupportedCurrenciesResponseDto.md)
- [SyncLoginDto](docs/Model/SyncLoginDto.md)
- [UpdateCheckoutLinkDto](docs/Model/UpdateCheckoutLinkDto.md)
- [UpdateCollectionDto](docs/Model/UpdateCollectionDto.md)
- [UpdateCollectionProductDto](docs/Model/UpdateCollectionProductDto.md)
- [UpdateCustomerDto](docs/Model/UpdateCustomerDto.md)
- [UpdateInstanceDto](docs/Model/UpdateInstanceDto.md)
- [UpdateMeterDto](docs/Model/UpdateMeterDto.md)
- [UpdateWebhookEndpointDto](docs/Model/UpdateWebhookEndpointDto.md)
- [WebhookDeliveryResponseDto](docs/Model/WebhookDeliveryResponseDto.md)
- [WebhookDisputePayload](docs/Model/WebhookDisputePayload.md)
- [WebhookEndpointResponseDto](docs/Model/WebhookEndpointResponseDto.md)
- [WebhookEntitlementGrantPayload](docs/Model/WebhookEntitlementGrantPayload.md)
- [WebhookLicensePayload](docs/Model/WebhookLicensePayload.md)
- [WebhookPaymentPayload](docs/Model/WebhookPaymentPayload.md)
- [WebhookPaymentPayloadBillingAddress](docs/Model/WebhookPaymentPayloadBillingAddress.md)
- [WebhookRefundPayload](docs/Model/WebhookRefundPayload.md)
- [WebhookSubscriptionPayload](docs/Model/WebhookSubscriptionPayload.md)

## Authorization

Authentication schemes defined for the API:
### ApiKeyAuth

- **Type**: Bearer authentication (API Key)

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `1.0.0`
    - Generator version: `7.10.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
