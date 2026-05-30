# Solifyn::Withdrawal

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The local withdrawal ID |  |
| **whop_id** | **String** | The Whop withdrawal ID |  |
| **amount** | **Float** | The amount withdrawn in cents |  |
| **currency** | **String** | Three-letter ISO currency code |  |
| **status** | **String** | The status of the withdrawal request |  |
| **fee_amount** | **Float** | Fee amount charged for the withdrawal in cents | [optional] |
| **fee_type** | **String** | The fee structure type (inclusive or exclusive) | [optional] |
| **markup_fee** | **Float** | Markup fee applied in cents | [optional] |
| **speed** | **String** | Speed of withdrawal (standard, instant) | [optional] |
| **trace_code** | **String** | Bank trace or reference code for tracking the payout | [optional] |
| **payer_name** | **String** | The name of the entity or account paying out | [optional] |
| **error_message** | **String** | Error message if the withdrawal failed | [optional] |
| **business_id** | **String** | The business ID associated with this withdrawal |  |
| **created_at** | **Time** | Timestamp when the withdrawal was requested |  |
| **updated_at** | **Time** | Timestamp when the withdrawal status was updated |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::Withdrawal.new(
  id: wd_123,
  whop_id: wdrl_123,
  amount: 1000,
  currency: usd,
  status: completed,
  fee_amount: 150,
  fee_type: exclusive,
  markup_fee: 50,
  speed: standard,
  trace_code: TR123456789,
  payer_name: Whop Payments,
  error_message: Insufficient funds in balance,
  business_id: biz_123,
  created_at: 2025-01-01T12:00:00Z,
  updated_at: 2025-01-01T12:00:00Z
)
```

