# # SubscriptionAction

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**free_days** | **float** | Number of free days to add (used with action: add_free_days) | [optional]
**cancellation_mode** | **string** | Cancellation mode (used with action: cancel) | [optional]
**void_payments** | **bool** | Whether to void subsequent payments (used with action: pause) | [optional]
**addon_product_id** | **string** | ID of the addon product to adjust seats for (used with action: adjust_seats) | [optional]
**new_quantity** | **float** | The new seat quantity (used with action: adjust_seats) | [optional]
**proration_type** | **string** | Proration strategy mode (used with action: adjust_seats) | [optional]
**idempotency_key** | **string** | A unique idempotency key to prevent duplicate mutative actions for network transient retries. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
