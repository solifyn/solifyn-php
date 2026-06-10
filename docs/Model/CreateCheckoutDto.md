# # CreateCheckoutDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**product_id** | **string** | The public product identifier (product ID) |
**currency** | **string** | Three-letter ISO currency code (lowercase) | [optional]
**quantity** | **float** | The quantity of items to buy | [optional] [default to 1]
**discount_code** | **string** | Discount code to apply | [optional]
**custom_price** | **float** | Custom price paid by customer (for Pay What You Want products) | [optional]
**customer_email** | **string** | Email address of the customer | [optional]
**checkout_data** | **object** | JSON metadata or checkout custom information | [optional]
**custom_fields** | **object** | Custom text fields required for the purchase | [optional]
**aff** | **string** | Affiliate partner tracking code | [optional]
**checkout_id** | **string** | The existing checkout database ID to validate / update | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
