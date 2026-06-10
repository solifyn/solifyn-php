# # License

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique prefix-based identifier of the license key. |
**key** | **string** | The cryptographically generated license key string delivered to the customer. |
**status** | **string** | Lifecycle status of the license. ACTIVE &#x3D; active. DISABLED &#x3D; suspended. REVOKED &#x3D; hard-revoked. |
**business_id** | **string** | The unique identifier associated with the business this license belongs to. |
**product_id** | **string** | The unique ID of the product this license key is associated with. |
**payment_id** | **string** | The unique payment identifier that triggered the issuance of this license key. |
**customer_id** | **string** | The unique customer identifier (ID) who received this license key. |
**activation_limit** | **float** | Maximum number of simultaneous active device instances allowed for this license. Null means unlimited. |
**activation_message** | **string** | Optional message displayed to the customer upon successful activation. |
**instances_count** | **float** | Running count of how many times this license key has been activated. |
**expiry_hours** | **float** | Relative expiry duration in hours from the time of issuance. |
**expires_at** | **string** | Absolute expiration timestamp. The license becomes invalid after this point. |
**filters** | **object** | Optional custom metadata filters associated with the license. |
**archived** | **bool** | Indicates if the license key is archived. |
**created_at** | **string** | Timestamp indicating exactly when the license key was issued. |
**updated_at** | **string** | Timestamp indicating when the license key was last modified. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
