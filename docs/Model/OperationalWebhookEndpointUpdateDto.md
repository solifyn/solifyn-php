# # OperationalWebhookEndpointUpdateDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **string** | The URL to send webhook events to. |
**description** | **string** | Optional description for the endpoint. | [optional]
**disabled** | **bool** | Whether the endpoint is disabled. | [optional]
**filter_types** | **string[]** | The operational event types this endpoint will receive. | [optional]
**metadata** | **object** | Metadata key-value pairs associated with the endpoint. | [optional]
**throttle_rate** | **float** | Maximum messages per second to send to this endpoint. | [optional]
**uid** | **string** | Optional unique user-defined identifier for the endpoint. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
