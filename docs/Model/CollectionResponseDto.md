# # CollectionResponseDto

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
**products** | [**\Solifyn\Model\CollectionProductRefDto[]**](CollectionProductRefDto.md) | List of product references (id + quantity). Full product details are available via GET /products/:id. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
