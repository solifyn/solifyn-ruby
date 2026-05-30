# Solifyn::CollectionProductEntry

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The product ID (whopId or internal database ID) |  |
| **quantity** | **Float** | Quantity of this product in the collection. Required, defaults to 1. | [default to 1] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::CollectionProductEntry.new(
  id: prod_123,
  quantity: 1
)
```

