# Solifyn::OrderDetail

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **files_snapshot** | **Array&lt;String&gt;** | Snapshot of files accessible after payment. | [optional] |
| **license_key** | **String** | Assigned license key, if applicable. | [optional] |
| **status** | **String** | Order resolution status. | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::OrderDetail.new(
  files_snapshot: null,
  license_key: FYN-XXXX-YYYY,
  status: completed
)
```

