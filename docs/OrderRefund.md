# Solifyn::OrderRefund

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **refund_id** | **String** | Unique refund identifier. |  |
| **payment_id** | **String** | Associated payment ID. |  |
| **amount** | **Integer** | Refunded amount in cents. |  |
| **currency** | **String** | Currency code. |  |
| **status** | **String** | Status of refund. |  |
| **reason** | **String** | Reason for refund. | [optional] |
| **is_partial** | **Boolean** | Whether it is a partial refund. |  |
| **created_at** | **Time** | Refund creation timestamp. |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::OrderRefund.new(
  refund_id: ref_123,
  payment_id: pay_123,
  amount: 1000,
  currency: usd,
  status: succeeded,
  reason: requested_by_customer,
  is_partial: true,
  created_at: 2026-05-22T08:00Z
)
```

