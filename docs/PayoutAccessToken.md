# Solifyn::PayoutAccessToken

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **access_token** | **String** | The temporary access token for embed portals |  |
| **expires_at** | **Time** | Expiration timestamp of the access token |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::PayoutAccessToken.new(
  access_token: token_abc123,
  expires_at: 2025-01-01T13:00:00Z
)
```

