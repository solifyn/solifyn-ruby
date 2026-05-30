# Solifyn::MeterQuantitiesCostDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **String** | The product ID attached to the meter. |  |
| **total_usage** | **Float** | Total usage in the requested date range. |  |
| **billable_usage** | **Float** | Billable usage after free threshold is applied. |  |
| **cost** | **Float** | Calculated cost for this product. |  |
| **currency** | **String** | Currency used for the cost calculation. |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::MeterQuantitiesCostDto.new(
  product_id: prod_9z8x7c6v5b4n,
  total_usage: 1540,
  billable_usage: 1500,
  cost: 19.5,
  currency: USD
)
```

