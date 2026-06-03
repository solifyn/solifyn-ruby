# Solifyn::OperationalWebhookEndpointResponseDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **url** | **String** |  |  |
| **description** | **String** |  |  |
| **disabled** | **Boolean** |  |  |
| **filter_types** | **Array&lt;String&gt;** |  |  |
| **metadata** | **Object** |  | [optional] |
| **throttle_rate** | **Float** |  |  |
| **uid** | **Object** |  | [optional] |
| **created_at** | **Time** |  |  |
| **updated_at** | **Time** |  |  |
| **secret** | **String** | The endpoint&#39;s raw secret (only returned on POST creation). | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::OperationalWebhookEndpointResponseDto.new(
  id: ep_1srOrx2ZWZBpBUvZwXKQmoEYga2,
  url: https://example.com/webhook/,
  description: Production monitoring endpoint,
  disabled: false,
  filter_types: [message.attempt.failing],
  metadata: {environment&#x3D;production},
  throttle_rate: 0,
  uid: monitoring-prod-endpoint,
  created_at: 2026-05-30T14:11:29.071Z,
  updated_at: 2026-05-30T14:11:29.071Z,
  secret: whsec_C2FVsBQIhrscChlQIMV+b5sSYspob7oD
)
```

