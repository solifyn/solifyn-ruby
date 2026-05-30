# Solifyn::OrderList

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **items** | [**Array&lt;Order&gt;**](Order.md) | List of order items. |  |
| **total_count** | **Integer** | Total number of items matching filters. |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::OrderList.new(
  items: null,
  total_count: 120
)
```

