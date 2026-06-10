# Solifyn::AddonCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **String** | The product ID of the addon product. |  |
| **min_quantity** | **Float** | Minimum quantity of the addon allowed to be purchased. | [default to 0] |
| **max_quantity** | **Float** | Maximum quantity of the addon allowed to be purchased (optional). | [optional] |
| **price_override** | **Float** | Price override for the addon product when purchased with this parent (optional). | [optional] |
| **is_seat_addon** | **Boolean** | Flag indicating if this addon represents a seat/license limit increment. | [default to false] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::AddonCreate.new(
  product_id: prod_addon_123,
  min_quantity: 0,
  max_quantity: 10,
  price_override: 15,
  is_seat_addon: true
)
```

