# Solifyn::OperationalWebhookEndpointHeadersInDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **headers** | **Object** | Custom key-value headers to send with the webhook. |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::OperationalWebhookEndpointHeadersInDto.new(
  headers: {X-Example&#x3D;123, X-Foobar&#x3D;Bar}
)
```

