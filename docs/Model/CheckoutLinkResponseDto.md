# # CheckoutLinkResponseDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The checkout link ID |
**title** | **string** | The title of the checkout link | [optional]
**product_id** | **string** | The linked Product ID | [optional]
**collection_id** | **string** | The linked Collection ID | [optional]
**customer_name** | **string** | Pre-filled customer name | [optional]
**customer_email** | **string** | Pre-filled customer email | [optional]
**address_line1** | **string** | Pre-filled address line 1 | [optional]
**city** | **string** | Pre-filled city | [optional]
**state** | **string** | Pre-filled state | [optional]
**postal_code** | **string** | Pre-filled postal code | [optional]
**country** | **string** | Pre-filled country | [optional]
**quantity** | **float** | Quantity to purchase |
**redirect_url** | **string** | URL to redirect to after successful payment | [optional]
**cancel_url** | **string** | URL to redirect to if payment is cancelled | [optional]
**show_discounts** | **bool** | Whether to show discounts on the checkout page |
**created_at** | **\DateTime** | Timestamp when the link was created |
**updated_at** | **\DateTime** | Timestamp when the link was last updated |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
