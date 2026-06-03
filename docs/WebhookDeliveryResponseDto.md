# Solifyn::WebhookDeliveryResponseDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **endpoint_id** | **String** |  |  |
| **event** | **String** |  |  |
| **payload** | **Object** |  |  |
| **response_status** | **Object** |  | [optional] |
| **response_body** | **Object** |  | [optional] |
| **duration_ms** | **Object** |  | [optional] |
| **status** | **String** |  |  |
| **created_at** | **Time** |  |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::WebhookDeliveryResponseDto.new(
  id: dlv_12345,
  endpoint_id: ep_12345,
  event: payment.succeeded,
  payload: {type&#x3D;payment.succeeded, data&#x3D;{}},
  response_status: 200,
  response_body: {&quot;success&quot;:true},
  duration_ms: 120,
  status: SUCCESS,
  created_at: 2026-05-30T14:11:29.071Z
)
```

