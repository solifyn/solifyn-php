# # SubscriptionSeatAdjustment

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** | Indicates if the seat adjustment was successful |
**subscription_id** | **string** | The customer subscription ID |
**addon_product_id** | **string** | The unique ID of the addon product |
**old_quantity** | **float** | The previous seat quantity |
**new_quantity** | **float** | The new seat quantity after adjustment |
**quantity_delta** | **float** | The difference in seat quantity |
**proration_type** | **string** | The proration strategy type applied |
**cost_impact** | **float** | Calculated pro-rata price cost impact in currency unit (charged or credited) |
**currency** | **string** | Billing currency |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
