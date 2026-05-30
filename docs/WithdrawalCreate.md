# Solifyn::WithdrawalCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **amount** | **Float** | The amount to withdraw in cents (e.g. 1000 for $10.00) |  |
| **currency** | **String** | Three-letter ISO currency code (lowercase) |  |
| **payout_method_id** | **String** | The ID of the payout method to withdraw to. If omitted, default is used. | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::WithdrawalCreate.new(
  amount: 1000,
  currency: usd,
  payout_method_id: pm_123
)
```

