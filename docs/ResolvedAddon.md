# Solifyn::ResolvedAddon

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **String** | Unique product ID of the addon |  |
| **name** | **String** | Display name of the addon |  |
| **image_url** | **Object** | URL of the addon image |  |
| **quantity** | **Float** | The purchased quantity of the addon |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::ResolvedAddon.new(
  product_id: prod_addon_123,
  name: Extra Seats add-on,
  image_url: null,
  quantity: 3
)
```

