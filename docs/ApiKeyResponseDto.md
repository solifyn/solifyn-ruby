# Solifyn::ApiKeyResponseDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **name** | **String** |  |  |
| **prefix** | **String** |  |  |
| **status** | **String** |  |  |
| **allow_write** | **Boolean** |  |  |
| **api_key** | **String** | The raw API key. Only returned once during creation. | [optional] |
| **expires_at** | **Time** |  |  |
| **last_used_at** | **Object** |  | [optional] |
| **created_at** | **Time** |  |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::ApiKeyResponseDto.new(
  id: key_019e56a1...,
  name: Production Key,
  prefix: fyn,
  status: ACTIVE,
  allow_write: true,
  api_key: fyn_key_123456...,
  expires_at: 2036-05-30T14:11:29.071Z,
  last_used_at: 2026-05-30T14:11:29.071Z,
  created_at: 2026-05-30T14:11:29.071Z
)
```

