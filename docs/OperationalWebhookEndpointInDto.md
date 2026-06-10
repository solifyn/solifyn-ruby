# Solifyn::OperationalWebhookEndpointInDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | The URL to send webhook events to. |  |
| **description** | **String** | Optional description for the endpoint. | [optional] |
| **disabled** | **Boolean** | Whether the endpoint is disabled. | [optional][default to false] |
| **filter_types** | **Array&lt;String&gt;** | The operational event types this endpoint will receive. | [optional] |
| **metadata** | **Object** | Metadata key-value pairs associated with the endpoint. | [optional] |
| **secret** | **String** | Optional custom endpoint signing secret (base64 encoded random bytes optionally prefixed with whsec_). If not set, the server will generate one. | [optional] |
| **throttle_rate** | **Float** | Maximum messages per second to send to this endpoint (outgoing messages will be throttled to this rate). | [optional] |
| **uid** | **String** | Optional unique user-defined identifier for the endpoint. | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::OperationalWebhookEndpointInDto.new(
  url: https://example.com/webhook/,
  description: Production monitoring endpoint,
  disabled: false,
  filter_types: [&quot;message.attempt.failing&quot;,&quot;message.attempt.exhausted&quot;],
  metadata: {&quot;environment&quot;:&quot;production&quot;},
  secret: whsec_C2FVsBQIhrscChlQIMV+b5sSYspob7oD,
  throttle_rate: 5,
  uid: monitoring-prod-endpoint
)
```

