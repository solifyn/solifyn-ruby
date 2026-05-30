# Solifyn::PayoutAccountLink

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | The URL redirecting to the Stripe Express onboarding/portal |  |
| **expires_at** | **Time** | Expiration timestamp of the link |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::PayoutAccountLink.new(
  url: https://connect.stripe.com/express/oauth/authorize...,
  expires_at: 2025-01-01T12:30:00Z
)
```

