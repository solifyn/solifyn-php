# # Dispute

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The dispute ID |
**whop_id** | **string** | The Whop Dispute ID |
**amount** | **float** | The dispute amount |
**currency** | **string** | The currency code |
**status** | **string** | The status of the dispute |
**reason** | **string** | The reason for the dispute | [optional]
**editable** | **bool** | Whether the evidence is still editable |
**needs_response_by** | **\DateTime** | Timestamp by when evidence must be submitted | [optional]
**visa_rdr** | **bool** | Whether Visa RDR was applied |
**billing_address** | **string** | Customer billing address details | [optional]
**customer_name** | **string** | Customer name | [optional]
**customer_email** | **string** | Customer email address | [optional]
**notes** | **string** | Additional notes | [optional]
**product_description** | **string** | Product or service description | [optional]
**service_date** | **string** | Service or purchase date | [optional]
**access_activity_log** | **string** | Log of access activity | [optional]
**evidence** | [**\Solifyn\Model\DisputeEvidenceDto**](DisputeEvidenceDto.md) | Evidence attachments associated with the dispute | [optional]
**payment_id** | **string** | The associated payment ID |
**business_id** | **string** | The associated business ID |
**created_at** | **\DateTime** | Timestamp when the dispute was created |
**updated_at** | **\DateTime** | Timestamp when the dispute was last updated |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
