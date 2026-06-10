# Solifyn::MeterResponseDto

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

## Example

```ruby
require 'solifyn'

instance = Solifyn::MeterResponseDto.new(
  id: mtr_8Z1aB2cD3eF4gH5iJ6kL7m,
  business_id: biz_4r5t6y7u8i9o,
  name: API Request Count,
  description: Counts successful API requests for usage-based billing.,
  event_name: api.request,
  aggregation_type: COUNT,
  aggregation_key: tokens,
  unit: requests,
  filters: {&quot;event_type&quot;:&quot;premium&quot;,&quot;region&quot;:&quot;asia&quot;},
  archived: false,
  created_at: 2026-05-23T10:00:00.000Z,
  updated_at: 2026-05-23T10:00:00.000Z
)
```

