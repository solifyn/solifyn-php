# # UpdateEntitlementDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | The user-friendly name of the entitlement | [optional]
**type** | **string** | The type of access to grant | [optional]
**github_repo** | **string** | The GitHub repository (e.g., owner/repo) | [optional]
**github_permission** | **string** | The GitHub repository permission level | [optional] [default to 'pull']
**discord_guild_id** | **string** | The Discord Guild/Server ID | [optional]
**discord_role_id** | **string** | The Discord Role ID to assign | [optional]
**framer_template_id** | **string** | The associated Framer Template ID | [optional]
**license_key** | **string** | The static License Key (if not dynamically generated) | [optional]
**activation_limit** | **float** | The maximum activation limit for licenses | [optional]
**activation_message** | **string** | A message shown to the user upon license activation | [optional]
**expiry_hours** | **float** | The number of hours until the entitlement expires | [optional]
**digital_link** | **string** | The digital download URL or redirect link | [optional]
**instructions** | **string** | Custom setup instructions for the user | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
