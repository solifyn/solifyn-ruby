# Solifyn::UpdateCustomerDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | The customer friendly full name | [optional] |
| **phone** | **String** | The customer telephone/phone number | [optional] |
| **username** | **String** | The username of the customer (e.g. Discord, Whop) | [optional] |
| **metadata** | **Object** | Custom key-value metadata associated with the customer | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::UpdateCustomerDto.new(
  name: John Doe,
  phone: +1234567890,
  username: johndoe,
  metadata: {customKey&#x3D;customValue}
)
```

