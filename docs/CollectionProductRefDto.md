# Solifyn::CollectionProductRefDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The public product identifier (whopId or internal ID) |  |
| **quantity** | **Float** | Quantity of this product in the collection |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::CollectionProductRefDto.new(
  id: prod_NG0mkkz0Awitk,
  quantity: 1
)
```

