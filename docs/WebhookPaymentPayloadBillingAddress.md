# Solifyn::WebhookPaymentPayloadBillingAddress

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  | [optional] |
| **line1** | **String** |  | [optional] |
| **line2** | **String** |  | [optional] |
| **city** | **String** |  | [optional] |
| **state** | **String** |  | [optional] |
| **country** | **String** |  | [optional] |
| **postal_code** | **String** |  | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::WebhookPaymentPayloadBillingAddress.new(
  name: null,
  line1: null,
  line2: null,
  city: null,
  state: null,
  country: null,
  postal_code: null
)
```

