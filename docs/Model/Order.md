# # Order

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique internal database identifier. |
**invoice_url** | **string** | The invoice print URL. |
**customer** | [**\Solifyn\Model\OrderCustomer**](OrderCustomer.md) | Customer details. |
**total_amount** | **int** | Total paid amount in cents. |
**subtotal** | **int** | Subtotal amount in cents. |
**usd_total** | **float** | Total paid amount converted to USD. | [optional]
**tax_amount** | **int** | Tax amount in cents. |
**application_fee** | **int** | Application fee in cents. |
**amount_after_fees** | **int** | Net amount after fees in cents. |
**currency** | **string** | Currency code. |
**status** | **string** | Current status of the payment. |
**created_at** | **\DateTime** | Payment creation timestamp. |
**paid_at** | **\DateTime** | Payment completion/paid timestamp. | [optional]
**payment_method** | **string** | Payment method utilized. |
**card_last_four** | **string** | Last four digits of card used. | [optional]
**card_network** | **string** | Card network/brand. | [optional]
**card_type** | **string** | Card type. | [optional]
**billing** | [**\Solifyn\Model\OrderBilling**](OrderBilling.md) | Billing address details. | [optional]
**product_cart** | [**\Solifyn\Model\OrderProductCart[]**](OrderProductCart.md) | Products purchased in this order. |
**metadata** | **object** | Custom metadata payload associated with this payment. | [optional]
**order** | [**\Solifyn\Model\OrderDetail**](OrderDetail.md) | Order details snapshot. | [optional]
**refundable** | **bool** | Indicates whether the order is eligible for refund. |
**refunds** | [**\Solifyn\Model\OrderRefund[]**](OrderRefund.md) | List of refunds associated with this payment. | [optional]
**business_id** | **string** | Business unique ID identifier. |
**business_name** | **string** | Business display title/name. |
**billing_reason** | **string** | Billing reason detail. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
