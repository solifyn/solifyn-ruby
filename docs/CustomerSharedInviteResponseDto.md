# Solifyn::CustomerSharedInviteResponseDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **token** | **String** | The generated invite token |  |
| **expires_at** | **Time** | The expiration timestamp of the token |  |
| **url** | **String** | The self-service shared portal URL | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::CustomerSharedInviteResponseDto.new(
  token: 2jb5bp8bq0jfucv7rtt9a8,
  expires_at: 2025-01-02T12:00Z,
  url: http://localhost:3000/shared/2jb5bp8bq0jfucv7rtt9a8
)
```

