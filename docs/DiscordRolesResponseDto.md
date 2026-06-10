# Solifyn::DiscordRolesResponseDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The Discord Role ID |  |
| **name** | **String** | The Discord Role Name |  |
| **position** | **Float** | The position of the role in the server hierarchy |  |
| **color** | **Float** | The color of the role (hex integer code) |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::DiscordRolesResponseDto.new(
  id: 876543210987654321,
  name: VIP Member,
  position: 3,
  color: 3447003
)
```

