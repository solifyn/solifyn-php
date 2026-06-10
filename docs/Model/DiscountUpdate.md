# # DiscountUpdate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Customer-facing name of the discount. | [optional]
**type** | **string** | Calculation type: percentage or fixed_amount. | [optional]
**amount** | **float** | The discount value. | [optional]
**usage_limit** | **int** | Maximum number of redemptions allowed. | [optional]
**expires_at** | **\DateTime** | Expiration timestamp for the discount. | [optional]
**subscription_cycles** | **int** | Number of subscription cycles this discount applies to. | [optional]
**restricted_to** | **string[]** | List of product IDs this discount is restricted to. | [optional]
**preserve_on_plan_change** | **bool** | Whether to preserve the discount when subscription plan changes. | [optional]
**metadata** | **object** | Custom metadata for the discount. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
