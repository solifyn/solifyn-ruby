# Solifyn::BusinessFullCreateResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **success** | **Boolean** | Indicates if creation was successful |  |
| **business_id** | **String** | The newly created business ID |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::BusinessFullCreateResponse.new(
  success: true,
  business_id: biz_123
)
```

