# Solifyn::PayoutVerification

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The verification check ID |  |
| **status** | **String** | Status of verification (pending, verified, rejected) |  |
| **type** | **String** | Verification type (identity, business, address) |  |
| **details** | **Object** | Details and requirements of the verification check | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::PayoutVerification.new(
  id: ver_123,
  status: verified,
  type: identity,
  details: null
)
```

