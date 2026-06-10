# Solifyn::MeterEventsResponseDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **meter_id** | **String** | The unique meter ID. |  |
| **items** | [**Array&lt;MeterUsageEventDto&gt;**](MeterUsageEventDto.md) | List of recent usage events. |  |
| **count** | **Float** | Number of returned usage events. |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::MeterEventsResponseDto.new(
  meter_id: mtr_8Z1aB2cD3eF4gH5iJ6kL7m,
  items: null,
  count: 100
)
```

