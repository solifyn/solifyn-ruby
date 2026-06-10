# Solifyn::OperationalWebhookEndpointSecretInDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **key** | **String** | Optional custom endpoint signing secret (base64 encoded random bytes optionally prefixed with whsec_). If not set, a new random secret is generated. | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::OperationalWebhookEndpointSecretInDto.new(
  key: whsec_C2FVsBQIhrscChlQIMV+b5sSYspob7oD
)
```

