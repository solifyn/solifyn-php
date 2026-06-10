# # WebhookEntitlementGrantPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique entitlement grant ID. | [optional]
**business_id** | **string** | The business ID context. | [optional]
**customer_id** | **string** | The customer ID. | [optional]
**payment_id** | **string** | Associated payment transaction ID. | [optional]
**product_id** | **string** | The purchased product ID. | [optional]
**type** | **string** | The type of entitlement (e.g. GITHUB). | [optional]
**github_repo** | **string** | Target GitHub repository (owner/repo) if type is GITHUB. | [optional]
**github_permission** | **string** | GitHub access permission level if type is GITHUB. | [optional]
**github_username** | **string** | The connected customer GitHub username. | [optional]
**status** | **string** | Delivery status of the collaborator invite (PENDING, DELIVERED, FAILED, REVOKED). | [optional]
**oauth_url** | **string** | OAuth URL to redirect the customer to. | [optional]
**error_details** | **string** | Error message if invitation delivery failed. | [optional]
**created_at** | **\DateTime** |  | [optional]
**updated_at** | **\DateTime** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
