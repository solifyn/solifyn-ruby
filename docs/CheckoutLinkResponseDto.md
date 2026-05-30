# Solifyn::CheckoutLinkResponseDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The checkout link ID |  |
| **title** | **String** | The title of the checkout link | [optional] |
| **product_id** | **String** | The linked Product ID | [optional] |
| **collection_id** | **String** | The linked Collection ID | [optional] |
| **customer_name** | **String** | Pre-filled customer name | [optional] |
| **customer_email** | **String** | Pre-filled customer email | [optional] |
| **address_line1** | **String** | Pre-filled address line 1 | [optional] |
| **city** | **String** | Pre-filled city | [optional] |
| **state** | **String** | Pre-filled state | [optional] |
| **postal_code** | **String** | Pre-filled postal code | [optional] |
| **country** | **String** | Pre-filled country | [optional] |
| **quantity** | **Float** | Quantity to purchase |  |
| **redirect_url** | **String** | URL to redirect to after successful payment | [optional] |
| **cancel_url** | **String** | URL to redirect to if payment is cancelled | [optional] |
| **show_discounts** | **Boolean** | Whether to show discounts on the checkout page |  |
| **created_at** | **Time** | Timestamp when the link was created |  |
| **updated_at** | **Time** | Timestamp when the link was last updated |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::CheckoutLinkResponseDto.new(
  id: chk_123,
  title: Winter Bundle Checkout,
  product_id: prod_123,
  collection_id: col_123,
  customer_name: John Doe,
  customer_email: customer@example.com,
  address_line1: 123 Main St,
  city: New York,
  state: NY,
  postal_code: 10001,
  country: US,
  quantity: 1,
  redirect_url: https://example.com/success,
  cancel_url: https://example.com/cancel,
  show_discounts: true,
  created_at: 2025-01-01T12:00:00Z,
  updated_at: 2025-01-01T12:00:00Z
)
```

