# Solifyn::Subscription

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique ID of the subscription |  |
| **status** | **String** | The status of the subscription (e.g. completed, active, trialing, past_due, canceled) |  |
| **created_at** | **Time** | Timestamp when the subscription was created |  |
| **joined_at** | **Time** | Timestamp when the member joined |  |
| **updated_at** | **Time** | Timestamp when the subscription was last updated |  |
| **manage_url** | **String** | The management URL for the billing/subscription |  |
| **member** | [**SubscriptionMemberDto**](SubscriptionMemberDto.md) | The member details |  |
| **user** | [**SubscriptionUserDto**](SubscriptionUserDto.md) | The user details |  |
| **renewal_period_start** | **Object** | Start timestamp of the current renewal period |  |
| **renewal_period_end** | **Object** | End timestamp of the current renewal period |  |
| **cancel_at_period_end** | **Boolean** | Whether the subscription is set to cancel at the end of the billing period |  |
| **cancel_option** | **Object** | The cancel option details |  |
| **cancellation_reason** | **Object** | The reason for cancellation |  |
| **canceled_at** | **Object** | Timestamp when the subscription was canceled |  |
| **currency** | **String** | The currency used for payments |  |
| **company** | [**SubscriptionCompanyDto**](SubscriptionCompanyDto.md) | The company context details |  |
| **plan** | [**SubscriptionPlanDto**](SubscriptionPlanDto.md) | The plan associated with this subscription |  |
| **promo_code** | **Object** | The promo code applied to the subscription |  |
| **product** | [**SubscriptionProductDto**](SubscriptionProductDto.md) | The product associated with the subscription |  |
| **license_key** | **Object** | The license key associated with this subscription |  |
| **metadata** | **Object** | Additional metadata for the subscription |  |
| **payment_collection_paused** | **Boolean** | Whether the payment collection is currently paused |  |
| **checkout_configuration_id** | **String** | The checkout configuration ID used |  |
| **price** | **Object** | The price/amount of the membership | [optional] |
| **type** | **Object** | The type of the membership plan | [optional] |
| **customer_id** | **Object** | The business customer ID | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::Subscription.new(
  id: mem_123,
  status: active,
  created_at: 2025-01-01T12:00:00.000Z,
  joined_at: 2025-01-01T12:00:00.000Z,
  updated_at: 2025-01-01T12:00:00.000Z,
  manage_url: https://example.com/billing/manage/mber_123,
  member: null,
  user: null,
  renewal_period_start: null,
  renewal_period_end: null,
  cancel_at_period_end: false,
  cancel_option: null,
  cancellation_reason: null,
  canceled_at: null,
  currency: usd,
  company: null,
  plan: null,
  promo_code: null,
  product: null,
  license_key: null,
  metadata: {&quot;is_usage_based&quot;:&quot;false&quot;},
  payment_collection_paused: false,
  checkout_configuration_id: ch_123,
  price: 99,
  type: renewal,
  customer_id: cust_123
)
```

