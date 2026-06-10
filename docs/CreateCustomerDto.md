# Solifyn::CreateCustomerDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **email** | **String** | The unique email of the customer |  |
| **name** | **String** | The customer friendly full name |  |
| **phone** | **String** | The customer telephone/phone number | [optional] |
| **username** | **String** | The username of the customer (e.g. Discord, Whop) | [optional] |
| **metadata** | **Object** | Custom key-value metadata associated with the customer | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::CreateCustomerDto.new(
  email: customer@gmail.com,
  name: John Doe,
  phone: +1234567890,
  username: johndoe,
  metadata: {&quot;customKey&quot;:&quot;customValue&quot;}
)
```

