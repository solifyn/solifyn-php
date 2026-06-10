# # OrderRefundCreate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount** | **int** | The refund amount in cents. If full refund is true, this can represent the total amount. |
**is_full_refund** | **bool** | Whether this is a full refund or a partial refund. |
**idempotency_key** | **string** | A unique idempotency key to prevent double refunds for transient network retries. |
**auto_revoke_seats** | **bool** | Whether to automatically revoke seat add-ons matching the refund amount. | [optional]
**revoke_seats** | [**\Solifyn\Model\RevokeSeatDto[]**](RevokeSeatDto.md) | List of specific addons and the quantities of seats to revoke. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
