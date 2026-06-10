# Solifyn::Addon

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **String** | The product ID of the addon product. |  |
| **min_quantity** | **Float** | Minimum quantity allowed. |  |
| **max_quantity** | **Object** | Maximum quantity allowed (null if unlimited). |  |
| **price_override** | **Object** | Price override (null if using base product price). |  |
| **is_seat_addon** | **Boolean** | Flag indicating if this is a seat/license addon. |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::Addon.new(
  product_id: prod_addon_123,
  min_quantity: 1,
  max_quantity: 10,
  price_override: 15,
  is_seat_addon: true
)
```

