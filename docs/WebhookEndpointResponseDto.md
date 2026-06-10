# Solifyn::WebhookEndpointResponseDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **url** | **String** |  |  |
| **description** | **String** |  |  |
| **events** | **Array&lt;String&gt;** |  |  |
| **status** | **String** |  |  |
| **masked_secret** | **String** | Masked signing secret for verification. |  |
| **secret** | **String** | Raw signing secret (only returned once during creation). | [optional] |
| **created_at** | **Time** |  |  |
| **updated_at** | **Time** |  | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::WebhookEndpointResponseDto.new(
  id: ep_12345,
  url: https://api.example.com/webhooks,
  description: Primary payment listener,
  events: [&quot;payment.created&quot;,&quot;payment.succeeded&quot;],
  status: ACTIVE,
  masked_secret: whsec_Ab...xyz,
  secret: whsec_AbCDeFGhiJKlMnOpQrStUvWxYz123456,
  created_at: 2026-05-30T14:11:29.071Z,
  updated_at: 2026-05-30T14:11:29.071Z
)
```

