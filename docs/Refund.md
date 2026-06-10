# Solifyn::Refund

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The refund ID |  |
| **whop_id** | **String** | The Whop Refund ID |  |
| **idempotency_key** | **String** | Client-generated key to prevent duplicate refunds | [optional] |
| **amount** | **Float** | Refunded amount |  |
| **currency** | **String** | Currency code |  |
| **status** | **String** | Status of the refund |  |
| **provider** | **String** | The payment provider used | [optional] |
| **reason** | **String** | Reason for the refund | [optional] |
| **reference_value** | **String** | Acquirer Reference Number (ARN) or tracking number | [optional] |
| **payment_id** | **String** | The associated Payment ID |  |
| **provider_created_at** | **Time** | Timestamp when the refund was processed by the provider | [optional] |
| **created_at** | **Time** | Timestamp when the refund was created in our system |  |
| **updated_at** | **Time** | Timestamp when the refund was last updated |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::Refund.new(
  id: null,
  whop_id: rf_xyz123,
  idempotency_key: idemp_abc123,
  amount: 10.5,
  currency: USD,
  status: succeeded,
  provider: stripe,
  reason: requested_by_customer,
  reference_value: ARN123456789,
  payment_id: null,
  provider_created_at: 2025-01-01T12:00Z,
  created_at: 2025-01-01T12:00Z,
  updated_at: 2025-01-01T12:00Z
)
```

