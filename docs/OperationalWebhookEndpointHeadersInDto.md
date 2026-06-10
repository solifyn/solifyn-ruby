# Solifyn::OperationalWebhookEndpointHeadersInDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **headers** | **Object** | Custom key-value headers to send with the webhook. |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::OperationalWebhookEndpointHeadersInDto.new(
  headers: {&quot;X-Example&quot;:&quot;123&quot;,&quot;X-Foobar&quot;:&quot;Bar&quot;}
)
```

