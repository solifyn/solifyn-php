# # CreateCheckoutLinkDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **string** | The friendly display title of this checkout link | [optional]
**product_id** | **string** | Product database/Whop ID to sell |
**collection_id** | **string** | Optional collection database ID to sell | [optional]
**customer_name** | **string** | Prefilled customer name for checkout inputs | [optional]
**customer_email** | **string** | Prefilled customer email for checkout inputs | [optional]
**address_line1** | **string** | Prefilled customer billing address line 1 | [optional]
**city** | **string** | Prefilled customer billing city | [optional]
**state** | **string** | Prefilled customer billing state | [optional]
**postal_code** | **string** | Prefilled customer billing zip/postal code | [optional]
**country** | **string** | Prefilled customer billing country (2-letter ISO) | [optional]
**quantity** | **object** | Override quantity for checkout session | [optional]
**redirect_url** | **string** | The absolute URL to redirect to upon successful payment completion | [optional]
**cancel_url** | **string** | The absolute URL to redirect to if a customer cancels the payment | [optional]
**show_discounts** | **bool** | Whether to display discount input form fields on checkout screen | [optional] [default to true]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
