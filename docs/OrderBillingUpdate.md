# Solifyn::OrderBillingUpdate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **street** | **String** |  | [optional] |
| **city** | **String** |  | [optional] |
| **state** | **String** |  | [optional] |
| **zipcode** | **String** |  | [optional] |
| **country** | **String** |  | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::OrderBillingUpdate.new(
  street: 123 Main St,
  city: San Francisco,
  state: CA,
  zipcode: 94105,
  country: US
)
```

