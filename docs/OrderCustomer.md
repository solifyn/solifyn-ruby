# Solifyn::OrderCustomer

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | The customer identifier. |  |
| **email** | **String** | The customer email address. |  |
| **name** | **String** | The customer name. |  |
| **username** | **String** | The customer username. | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::OrderCustomer.new(
  customer_id: usr_123,
  email: customer@example.com,
  name: John Doe,
  username: johndoe
)
```

