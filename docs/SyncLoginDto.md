# Solifyn::SyncLoginDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **live_token** | **String** | The JWT access token from the Live API server |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::SyncLoginDto.new(
  live_token: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...
)
```

