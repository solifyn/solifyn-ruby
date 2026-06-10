# Solifyn::AddonUpdate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **min_quantity** | **Float** | Minimum quantity of the addon allowed to be purchased. | [optional] |
| **max_quantity** | **Float** | Maximum quantity of the addon allowed to be purchased (optional). | [optional] |
| **price_override** | **Float** | Price override for the addon product when purchased with this parent (optional). | [optional] |
| **is_seat_addon** | **Boolean** | Flag indicating if this addon represents a seat/license limit increment. | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::AddonUpdate.new(
  min_quantity: 1,
  max_quantity: 10,
  price_override: 15,
  is_seat_addon: true
)
```

