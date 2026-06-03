# Solifyn::CreateApiKeyDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | The user-friendly name of the API key. |  |
| **allow_write** | **Boolean** | Whether the API key is allowed to make mutating write requests. | [optional][default to true] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::CreateApiKeyDto.new(
  name: Production Key,
  allow_write: true
)
```

