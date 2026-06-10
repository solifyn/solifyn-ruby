# Solifyn::CustomerListResponseDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **items** | [**Array&lt;CustomerResponseDto&gt;**](CustomerResponseDto.md) | List of customers |  |
| **total_count** | **Float** | Total count of customers matching the filters |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::CustomerListResponseDto.new(
  items: null,
  total_count: 1
)
```

