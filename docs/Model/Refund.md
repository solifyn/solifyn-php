# # Refund

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The refund ID |
**whop_id** | **string** | The Whop Refund ID |
**idempotency_key** | **string** | Client-generated key to prevent duplicate refunds | [optional]
**amount** | **float** | Refunded amount |
**currency** | **string** | Currency code |
**status** | **string** | Status of the refund |
**provider** | **string** | The payment provider used | [optional]
**reason** | **string** | Reason for the refund | [optional]
**reference_value** | **string** | Acquirer Reference Number (ARN) or tracking number | [optional]
**payment_id** | **string** | The associated Payment ID |
**provider_created_at** | **\DateTime** | Timestamp when the refund was processed by the provider | [optional]
**created_at** | **\DateTime** | Timestamp when the refund was created in our system |
**updated_at** | **\DateTime** | Timestamp when the refund was last updated |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
