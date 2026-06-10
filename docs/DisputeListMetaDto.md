# Solifyn::DisputeListMetaDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **total** | **Float** | Total count of disputes |  |
| **page** | **Float** | Current page number |  |
| **limit** | **Float** | Limit of items per page |  |
| **total_pages** | **Float** | Total number of pages |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::DisputeListMetaDto.new(
  total: 10,
  page: 1,
  limit: 10,
  total_pages: 1
)
```

