# Solifyn::CreateMeterDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Meter display name. |  |
| **description** | **String** | Meter description. | [optional] |
| **event_name** | **String** | The event name tracked by this meter. |  |
| **aggregation_type** | **String** | Aggregation strategy for usage events. |  |
| **aggregation_key** | **String** | Metadata key used by SUM, MAX, or LAST aggregation modes. | [optional] |
| **unit** | **String** | Measurement unit label. | [optional] |
| **filters** | **Hash&lt;String, Object&gt;** | Optional filter definition for advanced matching. | [optional] |
| **enable_filtering** | **Boolean** | Enable filtering on usage event ingestion. | [optional][default to false] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::CreateMeterDto.new(
  name: API Request Count,
  description: Counts successful API requests for usage-based billing.,
  event_name: api.request,
  aggregation_type: COUNT,
  aggregation_key: tokens,
  unit: requests,
  filters: {event_type&#x3D;premium, region&#x3D;asia},
  enable_filtering: false
)
```

