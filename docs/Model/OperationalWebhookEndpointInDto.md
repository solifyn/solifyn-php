# # OperationalWebhookEndpointInDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **string** | The URL to send webhook events to. |
**description** | **string** | Optional description for the endpoint. | [optional]
**disabled** | **bool** | Whether the endpoint is disabled. | [optional] [default to false]
**filter_types** | **string[]** | The operational event types this endpoint will receive. | [optional]
**metadata** | **object** | Metadata key-value pairs associated with the endpoint. | [optional]
**secret** | **string** | Optional custom endpoint signing secret (base64 encoded random bytes optionally prefixed with whsec_). If not set, the server will generate one. | [optional]
**throttle_rate** | **float** | Maximum messages per second to send to this endpoint (outgoing messages will be throttled to this rate). | [optional]
**uid** | **string** | Optional unique user-defined identifier for the endpoint. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
