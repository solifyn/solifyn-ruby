# Solifyn::WebhookRefundPayload

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Internal refund ID. | [optional] |
| **payment_id** | **String** |  | [optional] |
| **amount** | **String** | Dollar value, 2 d.p. | [optional] |
| **currency** | **String** |  | [optional] |
| **status** | **String** |  | [optional] |
| **reason** | **String** |  | [optional] |
| **reference_value** | **String** |  | [optional] |
| **provider** | **String** |  | [optional] |
| **provider_created_at** | **Time** |  | [optional] |
| **created_at** | **Time** |  | [optional] |
| **updated_at** | **Time** |  | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::WebhookRefundPayload.new(
  id: ref_abc123,
  payment_id: pay_019e60cb...,
  amount: 25.00,
  currency: USD,
  status: succeeded,
  reason: requested_by_customer,
  reference_value: null,
  provider: stripe,
  provider_created_at: null,
  created_at: null,
  updated_at: null
)
```

