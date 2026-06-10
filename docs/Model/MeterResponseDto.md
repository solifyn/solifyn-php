# # MeterResponseDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique meter ID. |
**business_id** | **string** | The business ID that owns this meter. |
**name** | **string** | Meter display name. |
**description** | **object** | Meter description. | [optional]
**event_name** | **string** | The event name tracked by this meter. |
**aggregation_type** | **string** | Aggregation strategy for usage events. |
**aggregation_key** | **object** | Metadata key used for aggregation. | [optional]
**unit** | **object** | Measurement unit label. | [optional]
**filters** | **array<string,mixed>** | Optional filter definition for advanced matching. | [optional]
**archived** | **bool** | Whether the meter is archived. |
**created_at** | **\DateTime** | Creation timestamp. |
**updated_at** | **\DateTime** | Last update timestamp. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
