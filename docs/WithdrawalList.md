# Solifyn::WithdrawalList

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **items** | [**Array&lt;Withdrawal&gt;**](Withdrawal.md) | List of withdrawals |  |
| **total_count** | **Float** | Total count of withdrawals matching filters |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::WithdrawalList.new(
  items: null,
  total_count: 5
)
```

