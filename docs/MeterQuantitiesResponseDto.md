# Solifyn::MeterQuantitiesResponseDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **meter_id** | **String** | The unique meter ID. |  |
| **name** | **String** | Meter display name. |  |
| **total_usage** | **Float** | Total usage within the selected time range. |  |
| **costs** | [**Array&lt;MeterQuantitiesCostDto&gt;**](MeterQuantitiesCostDto.md) | Cost breakdown for products attached to the meter. |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::MeterQuantitiesResponseDto.new(
  meter_id: mtr_8Z1aB2cD3eF4gH5iJ6kL7m,
  name: API Request Count,
  total_usage: 1540,
  costs: null
)
```

