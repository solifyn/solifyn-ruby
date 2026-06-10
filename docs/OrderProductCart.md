# Solifyn::OrderProductCart

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Product identifier. |  |
| **name** | **String** | Product name. |  |
| **quantity** | **Integer** | Quantity purchased. |  |
| **price** | **Integer** | Price per item in cents. |  |
| **pricing_type** | **String** | Pricing type, e.g. one-time or renewal. | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::OrderProductCart.new(
  id: prod_123,
  name: SaaS Pro Access,
  quantity: 1,
  price: 2900,
  pricing_type: one_time
)
```

