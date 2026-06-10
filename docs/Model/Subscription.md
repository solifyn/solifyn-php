# # Subscription

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique ID of the subscription |
**status** | **string** | The status of the subscription (e.g. completed, active, trialing, past_due, canceled) |
**created_at** | **\DateTime** | Timestamp when the subscription was created |
**joined_at** | **\DateTime** | Timestamp when the member joined |
**updated_at** | **\DateTime** | Timestamp when the subscription was last updated |
**manage_url** | **string** | The management URL for the billing/subscription |
**member** | [**\Solifyn\Model\SubscriptionMemberDto**](SubscriptionMemberDto.md) | The member details |
**user** | [**\Solifyn\Model\SubscriptionUserDto**](SubscriptionUserDto.md) | The user details |
**renewal_period_start** | **object** | Start timestamp of the current renewal period |
**renewal_period_end** | **object** | End timestamp of the current renewal period |
**cancel_at_period_end** | **bool** | Whether the subscription is set to cancel at the end of the billing period |
**cancel_option** | **object** | The cancel option details |
**cancellation_reason** | **object** | The reason for cancellation |
**canceled_at** | **object** | Timestamp when the subscription was canceled |
**currency** | **string** | The currency used for payments |
**company** | [**\Solifyn\Model\SubscriptionCompanyDto**](SubscriptionCompanyDto.md) | The company context details |
**plan** | [**\Solifyn\Model\SubscriptionPlanDto**](SubscriptionPlanDto.md) | The plan associated with this subscription |
**promo_code** | **object** | The promo code applied to the subscription |
**product** | [**\Solifyn\Model\SubscriptionProductDto**](SubscriptionProductDto.md) | The product associated with the subscription |
**license_key** | **object** | The license key associated with this subscription |
**metadata** | **object** | Additional metadata for the subscription |
**payment_collection_paused** | **bool** | Whether the payment collection is currently paused |
**checkout_configuration_id** | **string** | The checkout configuration ID used |
**price** | **object** | The price/amount of the membership | [optional]
**type** | **object** | The type of the membership plan | [optional]
**customer_id** | **object** | The business customer ID | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
