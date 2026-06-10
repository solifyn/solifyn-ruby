# Solifyn::CreateCheckoutDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **String** | The public product identifier (product ID) |  |
| **currency** | **String** | Three-letter ISO currency code (lowercase) | [optional] |
| **quantity** | **Float** | The quantity of items to buy | [optional][default to 1] |
| **discount_code** | **String** | Discount code to apply | [optional] |
| **custom_price** | **Float** | Custom price paid by customer (for Pay What You Want products) | [optional] |
| **customer_email** | **String** | Email address of the customer | [optional] |
| **checkout_data** | **Object** | JSON metadata or checkout custom information | [optional] |
| **custom_fields** | **Object** | Custom text fields required for the purchase | [optional] |
| **aff** | **String** | Affiliate partner tracking code | [optional] |
| **checkout_id** | **String** | The existing checkout database ID to validate / update | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::CreateCheckoutDto.new(
  product_id: prod_XXXXXXXXXXX,
  currency: usd,
  quantity: 1,
  discount_code: PROMO10,
  custom_price: 15,
  customer_email: customer@example.com,
  checkout_data: null,
  custom_fields: null,
  aff: partner_abc,
  checkout_id: 019e56ba-9832-72ae-XXXXXXXXXXX
)
```

