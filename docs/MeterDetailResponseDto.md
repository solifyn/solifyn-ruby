# Solifyn::MeterDetailResponseDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique meter ID. |  |
| **business_id** | **String** | The business ID that owns this meter. |  |
| **name** | **String** | Meter display name. |  |
| **description** | **Object** | Meter description. | [optional] |
| **event_name** | **String** | The event name tracked by this meter. |  |
| **aggregation_type** | **String** | Aggregation strategy for usage events. |  |
| **aggregation_key** | **Object** | Metadata key used for aggregation. | [optional] |
| **unit** | **Object** | Measurement unit label. | [optional] |
| **filters** | **Hash&lt;String, Object&gt;** | Optional filter definition for advanced matching. | [optional] |
| **archived** | **Boolean** | Whether the meter is archived. |  |
| **created_at** | **Time** | Creation timestamp. |  |
| **updated_at** | **Time** | Last update timestamp. |  |
| **usage_events** | [**Array&lt;MeterUsageEventDto&gt;**](MeterUsageEventDto.md) | Most recent usage events recorded for the meter. |  |
| **total_usage_events** | **Float** | Total usage event count for the meter. |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::MeterDetailResponseDto.new(
  id: mtr_8Z1aB2cD3eF4gH5iJ6kL7m,
  business_id: biz_4r5t6y7u8i9o,
  name: API Request Count,
  description: Counts successful API requests for usage-based billing.,
  event_name: api.request,
  aggregation_type: COUNT,
  aggregation_key: tokens,
  unit: requests,
  filters: {event_type&#x3D;premium, region&#x3D;asia},
  archived: false,
  created_at: 2026-05-23T10:00:00.000Z,
  updated_at: 2026-05-23T10:00:00.000Z,
  usage_events: null,
  total_usage_events: 1284
)
```

