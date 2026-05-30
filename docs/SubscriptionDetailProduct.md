# Solifyn::SubscriptionDetailProduct

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The product unique ID |  |
| **name** | **String** | The product name |  |
| **price** | **Float** | Product base price |  |
| **currency** | **String** | Base currency |  |
| **metadata** | **Object** | Metadata JSON payload | [optional] |
| **pricing_type** | **String** | Pricing type, e.g. one-time or renewal |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::SubscriptionDetailProduct.new(
  id: prod_123,
  name: My Pro Product,
  price: 99,
  currency: usd,
  metadata: {},
  pricing_type: renewal
)
```

