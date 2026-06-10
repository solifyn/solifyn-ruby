# Solifyn::OrderRefundCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **amount** | **Integer** | The refund amount in cents. If full refund is true, this can represent the total amount. |  |
| **is_full_refund** | **Boolean** | Whether this is a full refund or a partial refund. |  |
| **idempotency_key** | **String** | A unique idempotency key to prevent double refunds for transient network retries. |  |
| **auto_revoke_seats** | **Boolean** | Whether to automatically revoke seat add-ons matching the refund amount. | [optional] |
| **revoke_seats** | [**Array&lt;RevokeSeatDto&gt;**](RevokeSeatDto.md) | List of specific addons and the quantities of seats to revoke. | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::OrderRefundCreate.new(
  amount: 1000,
  is_full_refund: true,
  idempotency_key: ref_idem_98sdufhskjfsd,
  auto_revoke_seats: false,
  revoke_seats: null
)
```

