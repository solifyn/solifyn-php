# # CollectionDetailResponseDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The collection ID |
**name** | **string** | The name of the collection |
**description** | **string** | A brief description of the collection | [optional]
**image_url** | **string** | URL of the collection image | [optional]
**status** | **string** | Status of the collection |
**business_id** | **string** | The unique identifier of the business owning this collection. |
**is_permanently_deleted** | **bool** | Indicates if the collection has been permanently deleted. |
**created_at** | **\DateTime** | Timestamp when the collection was created |
**updated_at** | **\DateTime** | Timestamp when the collection was last updated |
**products** | [**\Solifyn\Model\CollectionProductDto[]**](CollectionProductDto.md) | Full product details including quantity for each item in the collection | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
