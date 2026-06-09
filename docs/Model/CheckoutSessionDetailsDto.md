# # CheckoutSessionDetailsDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Checkout session identifier |
**price** | **float** | Total purchase amount |
**currency** | **string** | ISO currency code of the purchase |
**store_name** | **string** | Title or name of the merchant/store selling the item |
**status** | **string** | Current status of the checkout session |
**billing_address** | **object** | Customer billing address details | [optional]
**custom_fields** | **object** | Custom fields collected during purchase | [optional]
**session_id** | **string** | The payment partner session ID | [optional]
**payment_id** | **string** | Database payment transaction ID | [optional]
**checkout_url** | **string** | Checkout session redirect URL if loaded in link mode | [optional]
**product** | [**\Solifyn\Model\Product**](Product.md) | The details of the product being purchased | [optional]
**entitlement_grants** | **object[]** | List of entitlement grants (e.g. GitHub repo invites) associated with this checkout. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
