# Solifyn::UpdateWebhookEndpointDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | The URL to send webhook events to. | [optional] |
| **description** | **String** | Optional description for the webhook endpoint. | [optional] |
| **events** | **Array&lt;String&gt;** | The list of subscribed event types. | [optional] |
| **status** | **String** | The status of the webhook endpoint. | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::UpdateWebhookEndpointDto.new(
  url: https://api.example.com/new-webhooks,
  description: Updated payment listener,
  events: [&quot;payment.created&quot;,&quot;payment.succeeded&quot;,&quot;refund.succeeded&quot;],
  status: ACTIVE
)
```

