# # EntitlementGrantResponseDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique entitlement grant ID. |
**business_id** | **string** | The business ID context. |
**customer_id** | **string** | The customer ID. |
**payment_id** | **string** | Associated payment transaction ID. | [optional]
**product_id** | **string** | The purchased product ID. |
**type** | **string** | The type of entitlement (e.g. GITHUB, DISCORD, TELEGRAM). |
**github_repo** | **string** | Target GitHub repository (owner/repo) if type is GITHUB. | [optional]
**github_permission** | **string** | GitHub access permission level if type is GITHUB. | [optional]
**github_username** | **string** | The connected customer GitHub username. | [optional]
**discord_guild_id** | **string** | Target Discord Guild ID if type is DISCORD. | [optional]
**discord_role_id** | **string** | Target Discord Role ID if type is DISCORD. | [optional]
**discord_username** | **string** | The connected customer Discord username. | [optional]
**discord_user_id** | **string** | The connected customer Discord user ID. | [optional]
**framer_template_id** | **string** | The Framer template ID if type is FRAMER. | [optional]
**framer_remix_link** | **string** | The single-use remix link generated for the customer if type is FRAMER. | [optional]
**status** | **string** | Delivery status of the collaborator invite (PENDING, DELIVERED, FAILED, REVOKED). |
**oauth_url** | **string** | OAuth URL to redirect the customer to. | [optional]
**error_details** | **string** | Error message if invitation delivery failed. | [optional]
**metadata** | **object** | Platform-specific metadata. | [optional]
**created_at** | **string** | Creation timestamp. |
**updated_at** | **string** | Modification timestamp. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
