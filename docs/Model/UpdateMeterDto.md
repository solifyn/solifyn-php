# # UpdateMeterDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Meter display name. | [optional]
**description** | **string** | Meter description. | [optional]
**event_name** | **string** | The event name tracked by this meter. | [optional]
**aggregation_type** | **string** | Aggregation strategy for usage events. | [optional]
**aggregation_key** | **string** | Metadata key used by SUM, MAX, or LAST aggregation modes. | [optional]
**unit** | **string** | Measurement unit label. | [optional]
**filters** | **array<string,mixed>** | Optional filter definition for advanced matching. | [optional]
**enable_filtering** | **bool** | Enable filtering on usage event ingestion. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
