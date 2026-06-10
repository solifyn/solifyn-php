# # ProductCreate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Product display name. |
**description** | **string** | A description of the product. | [optional]
**price** | **float** | Price value. |
**currency** | **string** | Product pricing currency. | [default to 'USD']
**image_url** | **string** | URL of the product cover image. | [optional]
**tax_category** | **string** | Tax classification. |
**discount** | **float** | Percentage or flat rate discount. | [optional]
**has_license_key** | **bool** | Whether to automatically issue license keys upon successful orders. | [optional] [default to false]
**has_digital_delivery** | **bool** | Whether the purchase includes downloadable files. | [optional] [default to false]
**has_github_access** | **bool** | Whether the purchase includes GitHub repository access. | [optional] [default to false]
**github_repo** | **string** | GitHub repository to grant access to (format: owner/repo). | [optional]
**github_permission** | **string** | GitHub collaborator permission level. | [optional]
**is_tax_inclusive** | **bool** | Whether tax is included in the base price. | [optional] [default to false]
**activation_limit** | **int** | Maximum concurrent activated instances allowed per license key. | [optional]
**brand_id** | **string** | Brand id for the product, if not provided will default to primary brand. | [optional]
**billing_period** | **int** | Billing period in days (for Subscription products). | [optional]
**trial_period_days** | **int** | Trial duration in days. | [optional]
**expiration_days** | **int** | Subscription expiration duration in days. | [optional]
**statement_descriptor** | **string** | Custom billing descriptor. | [optional]
**pay_what_you_want** | **bool** | Allow pay-what-you-want pricing. | [optional] [default to false]
**metadata** | **array<string,string>** | Developer key-value metadata pairs. | [optional]
**custom_fields** | [**\Solifyn\Model\ProductCreateCustomFieldsInner[]**](ProductCreateCustomFieldsInner.md) | Form field configurations to gather during checkout. | [optional]
**stock** | **int** | Initial stock quantity limit. | [optional]
**is_listed** | **bool** | Whether the product is publicly visible. | [optional] [default to true]
**is_free** | **bool** | Whether the product is free of charge. | [optional] [default to false]
**addons** | [**\Solifyn\Model\ProductCreateAddonsInner[]**](ProductCreateAddonsInner.md) | Product addons configurations. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
