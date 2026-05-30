# Solifyn::OrderBilling

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **street** | **String** | Street address. | [optional] |
| **city** | **String** | City. | [optional] |
| **state** | **String** | State or province. | [optional] |
| **zipcode** | **String** | Postal or ZIP code. | [optional] |
| **country** | **String** | Country code. | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::OrderBilling.new(
  street: 123 Main St,
  city: San Francisco,
  state: CA,
  zipcode: 94105,
  country: US
)
```

