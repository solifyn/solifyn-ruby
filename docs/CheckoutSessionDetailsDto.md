# Solifyn::CheckoutSessionDetailsDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Checkout session identifier |  |
| **price** | **Float** | Total purchase amount |  |
| **currency** | **String** | ISO currency code of the purchase |  |
| **store_name** | **String** | Title or name of the merchant/store selling the item |  |
| **status** | **String** | Current status of the checkout session |  |
| **billing_address** | **Object** | Customer billing address details | [optional] |
| **custom_fields** | **Object** | Custom fields collected during purchase | [optional] |
| **session_id** | **String** | The payment partner session ID | [optional] |
| **payment_id** | **String** | Database payment transaction ID | [optional] |
| **checkout_url** | **String** | Checkout session redirect URL if loaded in link mode | [optional] |
| **product** | [**Product**](Product.md) | The details of the product being purchased | [optional] |
| **entitlement_grants** | **Array&lt;Object&gt;** | List of entitlement grants (e.g. GitHub repo invites) associated with this checkout. | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::CheckoutSessionDetailsDto.new(
  id: ch_XXXXXXXXXXX,
  price: 10,
  currency: USD,
  store_name: Official Store,
  status: pending,
  billing_address: null,
  custom_fields: null,
  session_id: ch_XXXXXXXXX,
  payment_id: pay_XXXXXXXXX,
  checkout_url: https://solifyn.com/checkout/prod_XXXXXXXXX?checkout_id&#x3D;019e56ba-9832-72ae-XXXXXXXXXXX,
  product: null,
  entitlement_grants: null
)
```

