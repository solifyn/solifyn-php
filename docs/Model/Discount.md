# # Discount

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique prefix-based identifier of the discount (e.g., &#x60;disc_cs8f67sd7f6fw3fs&#x60;). |
**discount_id** | **string** | Alias for the unique identifier of the discount. |
**code** | **string** | The unique discount code (e.g. SAVE10) used during checkout. |
**name** | **string** | The customer-facing name of the discount code (e.g. Summer Sale). | [optional]
**type** | **string** | The discount calculation type: percentage or fixed_amount. |
**amount** | **int** | The discount value. For percentage type, it is in basis points (e.g. 1000 &#x3D; 10.00%). For fixed_amount type, it is in cents (e.g. 1000 &#x3D; $10.00). |
**usage_limit** | **int** | Maximum number of times this discount code can be redeemed. Null represents unlimited usage. |
**times_used** | **int** | The number of times this discount code has been successfully redeemed. |
**expires_at** | **\DateTime** | The expiration timestamp after which the discount code is no longer valid. |
**status** | **string** | The current status of the discount. |
**business_id** | **string** | The unique identifier associated with the business this discount belongs to. |
**created_at** | **\DateTime** | Timestamp indicating exactly when the discount was created. |
**updated_at** | **\DateTime** | Timestamp indicating when the discount was last updated. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
