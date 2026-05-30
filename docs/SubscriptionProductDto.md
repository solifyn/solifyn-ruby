# Solifyn::SubscriptionProductDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique ID of the product |  |
| **title** | **String** | The title/name of the product |  |
| **metadata** | **Object** | Additional metadata associated with the product | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::SubscriptionProductDto.new(
  id: prod_123,
  title: Product Name,
  metadata: {}
)
```

