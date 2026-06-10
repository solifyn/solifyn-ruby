# Solifyn::SubscriptionUserDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique ID of the user |  |
| **username** | **String** | The username of the user |  |
| **name** | **String** | The full name of the user |  |
| **email** | **String** | The email address of the user |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::SubscriptionUserDto.new(
  id: user_123,
  username: johndoe,
  name: John Doe,
  email: john.doe@example.com
)
```

