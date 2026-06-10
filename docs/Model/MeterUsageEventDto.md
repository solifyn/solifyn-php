# # MeterUsageEventDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique usage event ID. |
**meter_id** | **string** | The meter ID this event belongs to. |
**customer_id** | **string** | The customer ID associated with the usage event. |
**value** | **float** | Numeric usage value recorded for the event. |
**metadata** | **array<string,mixed>** | Optional event metadata. | [optional]
**timestamp** | **\DateTime** | Timestamp when the usage event occurred. |
**processed_at** | **\DateTime** | Timestamp when the usage event was processed. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
