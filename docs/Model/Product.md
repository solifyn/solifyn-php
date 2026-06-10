# # Product

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique identifier (ID) of the product. |
**name** | **string** | The display name of the product. |
**price** | **float** | The price amount of the product (e.g. 29.00). |
**currency** | **string** | The three-letter ISO currency code (e.g. USD, VND, EUR). |
**description** | **string** | A comprehensive rich text description of the product. | [optional]
**status** | **string** | The lifecycle status of the product (e.g. ACTIVE, ARCHIVED). |
**image_url** | **string** | URL of the product cover image. |
**tax_category** | **string** | The tax classification for the product. |
**pricing_type** | **string** | Pricing model of the product. |
**discount** | **float** | Discount value as a percentage or fixed amount. |
**has_license_key** | **bool** | Indicates if the product issues a cryptographically secure software license key upon checkout completion. |
**has_digital_delivery** | **bool** | Whether the product includes digital file downloads upon purchase. |
**has_github_access** | **bool** | Whether the product includes GitHub repository access. |
**github_repo** | **string** | GitHub repository to grant access to (format: owner/repo). |
**github_permission** | **string** | GitHub collaborator permission level. |
**is_tax_inclusive** | **bool** | Whether the product price already includes applicable sales taxes. |
**billing_period** | **int** | The subscription billing cycle interval in days (for subscription products). |
**trial_period_days** | **int** | Trial duration in days for subscription products. |
**expiration_days** | **int** | Automatic expiration period in days for the subscription entitlement. |
**statement_descriptor** | **string** | Custom text displayed on customer credit card statements for purchases of this product. |
**pay_what_you_want** | **bool** | Indicates if customers are allowed to enter a custom pricing amount at checkout. |
**metadata** | **array<string,string>** | Custom developer metadata key-value pairs associated with the product. |
**custom_fields** | **object[]** | Custom form field questions to ask the customer during checkout. |
**stock** | **int** | Available stock quantity, or null for unlimited inventory. |
**activation_limit** | **int** | Maximum number of simultaneous active instances/devices allowed per issued license key (applicable if hasLicenseKey is true). |
**is_listed** | **bool** | Defines if the product is listed publicly on the merchant&#39;s storefront template. |
**is_free** | **bool** | Whether the product is free. |
**created_at** | **\DateTime** | Timestamp indicating exactly when the product was created. |
**updated_at** | **\DateTime** | Timestamp indicating when the product was last modified. |
**is_permanently_deleted** | **bool** | Indicates if the product has been permanently deleted. |
**brand_id** | **string** | Optional brand identifier. |
**digital_link** | **string** | Secure link for digital delivery. |
**instructions** | **string** | Special instructions provided upon purchase. |
**activation_message** | **string** | Custom message displayed when a license key is activated. |
**expiry_hours** | **int** | Number of hours until the license key expires. |
**business_id** | **string** | The unique identifier of the business owning this product. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
