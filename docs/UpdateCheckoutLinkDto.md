# Solifyn::UpdateCheckoutLinkDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **title** | **String** | The friendly display title of this checkout link | [optional] |
| **product_id** | **String** | Product database/Whop ID to sell | [optional] |
| **collection_id** | **String** | Optional collection database ID to sell | [optional] |
| **customer_name** | **String** | Prefilled customer name for checkout inputs | [optional] |
| **customer_email** | **String** | Prefilled customer email for checkout inputs | [optional] |
| **address_line1** | **String** | Prefilled customer billing address line 1 | [optional] |
| **city** | **String** | Prefilled customer billing city | [optional] |
| **state** | **String** | Prefilled customer billing state | [optional] |
| **postal_code** | **String** | Prefilled customer billing zip/postal code | [optional] |
| **country** | **String** | Prefilled customer billing country (2-letter ISO) | [optional] |
| **quantity** | **Object** | Override quantity for checkout session | [optional] |
| **redirect_url** | **String** | The absolute URL to redirect to upon successful payment completion | [optional] |
| **cancel_url** | **String** | The absolute URL to redirect to if a customer cancels the payment | [optional] |
| **show_discounts** | **Boolean** | Whether to display discount input form fields on checkout screen | [optional][default to true] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::UpdateCheckoutLinkDto.new(
  title: Winter Bundle Checkout,
  product_id: prod_123,
  collection_id: col_123,
  customer_name: John Doe,
  customer_email: customer@gmail.com,
  address_line1: 123 Main St,
  city: San Francisco,
  state: CA,
  postal_code: 94111,
  country: US,
  quantity: 1,
  redirect_url: https://mysite.com/success,
  cancel_url: https://mysite.com/cancel,
  show_discounts: true
)
```

