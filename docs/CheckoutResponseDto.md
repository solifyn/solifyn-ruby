# Solifyn::CheckoutResponseDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique identifier for the checkout session in database |  |
| **session_id** | **String** | The unique session ID format for external clients |  |
| **checkout_url** | **String** | The public redirect URL to the custom payment steps page |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::CheckoutResponseDto.new(
  id: 019e56ba-9832-72ae-XXXXXXXXXXX,
  session_id: ch_XXXXXXXXXXXXXX,
  checkout_url: http://localhost:3000/checkout/test/prod_XXXXXXXXXXX?checkout_id&#x3D;019e56ba-9832-72ae-XXXXXXXXXX
)
```

