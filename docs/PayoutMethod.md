# Solifyn::PayoutMethod

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The payout method ID |  |
| **type** | **String** | Type of payout method (e.g. bank_account, stripe) |  |
| **status** | **String** | Status of the payout method |  |
| **details** | **Object** | Metadata and details of the bank/card associated | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::PayoutMethod.new(
  id: pm_123,
  type: bank_account,
  status: active,
  details: null
)
```

