# Solifyn::CreateSetupCheckoutDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **company_id** | **String** | The Whop/Stripe company ID context |  |
| **currency** | **String** | Currency for setup mode | [optional][default to &#39;usd&#39;] |
| **retry_payment_id** | **String** | Internal or Whop failed payment ID to retry | [optional] |
| **membership_id** | **String** | Membership ID to link setup checkout to for card updating | [optional] |
| **plan_id** | **String** | Plan ID to retry or renew | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::CreateSetupCheckoutDto.new(
  company_id: biz_xxxxxxxxxxxxxx,
  currency: usd,
  retry_payment_id: pay_xxxxxxxxxxxxxx,
  membership_id: mem_xxxxxxxxxxxxxx,
  plan_id: plan_xxxxxxxxxxxxx
)
```

