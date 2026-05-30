# Solifyn::CreateCollectionCheckoutDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **collection_id** | **String** | The database ID of the collection to checkout |  |
| **quantity** | **Float** | Quantity of collections to buy | [optional][default to 1] |
| **discount_code** | **String** | Discount code to apply | [optional] |
| **aff** | **String** | Affiliate tracking code | [optional] |
| **custom_fields** | **Object** | Custom text fields / selected addons | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::CreateCollectionCheckoutDto.new(
  collection_id: col_123,
  quantity: 1,
  discount_code: PROMO10,
  aff: partner_abc,
  custom_fields: null
)
```

