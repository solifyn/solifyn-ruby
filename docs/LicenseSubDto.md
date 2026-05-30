# Solifyn::LicenseSubDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **key** | **String** |  |  |
| **status** | **String** |  |  |
| **activation_limit** | **Float** |  |  |
| **activation_message** | **String** |  |  |
| **expires_at** | **String** |  |  |
| **product** | [**ProductSubDto**](ProductSubDto.md) |  | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::LicenseSubDto.new(
  id: null,
  key: null,
  status: null,
  activation_limit: null,
  activation_message: null,
  expires_at: null,
  product: null
)
```

