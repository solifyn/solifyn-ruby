# Solifyn::DiscountsList200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **items** | [**Array&lt;Discount&gt;**](Discount.md) |  |  |
| **total** | **Integer** | Total number of items matching filters. |  |
| **total_count** | **Integer** | Total number of items matching filters (alias). |  |
| **pagination** | [**DiscountsList200ResponsePagination**](DiscountsList200ResponsePagination.md) |  |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::DiscountsList200Response.new(
  items: null,
  total: null,
  total_count: null,
  pagination: null
)
```

