# Solifyn::PayoutAccount

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The payout account ID |  |
| **status** | **String** | Status of the payout account onboarding |  |
| **capabilities** | **Object** | Onboarding capability status flags (e.g., transfers, payouts) | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::PayoutAccount.new(
  id: acct_123,
  status: active,
  capabilities: null
)
```

