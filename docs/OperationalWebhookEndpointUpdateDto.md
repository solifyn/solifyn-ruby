# Solifyn::OperationalWebhookEndpointUpdateDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | The URL to send webhook events to. |  |
| **description** | **String** | Optional description for the endpoint. | [optional] |
| **disabled** | **Boolean** | Whether the endpoint is disabled. | [optional] |
| **filter_types** | **Array&lt;String&gt;** | The operational event types this endpoint will receive. | [optional] |
| **metadata** | **Object** | Metadata key-value pairs associated with the endpoint. | [optional] |
| **throttle_rate** | **Float** | Maximum messages per second to send to this endpoint. | [optional] |
| **uid** | **String** | Optional unique user-defined identifier for the endpoint. | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::OperationalWebhookEndpointUpdateDto.new(
  url: https://example.com/new-webhook/,
  description: Updated monitoring endpoint,
  disabled: true,
  filter_types: [message.attempt.failing, message.attempt.exhausted, endpoint.disabled],
  metadata: {environment&#x3D;staging},
  throttle_rate: 10,
  uid: monitoring-updated-endpoint
)
```

