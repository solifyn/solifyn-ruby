# Solifyn::ProductCreateAddonsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **String** |  | [optional] |
| **min_quantity** | **Integer** |  | [optional] |
| **max_quantity** | **Integer** |  | [optional] |
| **price_override** | **Float** |  | [optional] |
| **is_seat_addon** | **Boolean** |  | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::ProductCreateAddonsInner.new(
  product_id: null,
  min_quantity: null,
  max_quantity: null,
  price_override: null,
  is_seat_addon: null
)
```

