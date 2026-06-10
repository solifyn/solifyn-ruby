# Solifyn::CreateWebhookEndpointDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | The URL to send webhook events to. |  |
| **description** | **String** | Optional description for the webhook endpoint. | [optional] |
| **events** | **Array&lt;String&gt;** | The list of subscribed event types. |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::CreateWebhookEndpointDto.new(
  url: https://api.example.com/webhooks,
  description: Primary payment listener,
  events: [&quot;payment.created&quot;,&quot;payment.succeeded&quot;]
)
```

