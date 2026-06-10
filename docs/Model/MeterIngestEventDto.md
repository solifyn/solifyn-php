# # MeterIngestEventDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**event_id** | **string** | Unique usage event ID for idempotency. |
**customer_id** | **string** | Unique customer ID associated with the event. |
**event_name** | **string** | Event name that should match a meter eventName. |
**value** | **float** | Event quantity value. | [optional] [default to 1]
**metadata** | **array<string,mixed>** | Metadata attached to the usage event. | [optional]
**timestamp** | **string** | Timestamp of the event in ISO 8601 format. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
