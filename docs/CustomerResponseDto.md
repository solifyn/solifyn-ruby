# Solifyn::CustomerResponseDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The customer ID |  |
| **member_id** | **String** | The Membership ID associated with this customer | [optional] |
| **email** | **String** | The email address of the customer |  |
| **name** | **String** | The name of the customer | [optional] |
| **username** | **String** | The username of the customer | [optional] |
| **phone** | **String** | The phone number of the customer | [optional] |
| **phone_number** | **String** | The phone number of the customer | [optional] |
| **metadata** | **Object** | Additional metadata associated with the customer | [optional] |
| **created_at** | **Time** | Timestamp when the customer was created |  |
| **updated_at** | **Time** | Timestamp when the customer was last updated |  |
| **business_id** | **String** | The business ID associated with the customer |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::CustomerResponseDto.new(
  id: user_123,
  member_id: mem_123,
  email: customer@example.com,
  name: John Doe,
  username: johndoe,
  phone: +1234567890,
  phone_number: +1234567890,
  metadata: {&quot;key&quot;:&quot;value&quot;},
  created_at: 2025-01-01T12:00Z,
  updated_at: 2025-01-01T12:00Z,
  business_id: 537825c3-14d6-4173-b072-33f921416efc
)
```

