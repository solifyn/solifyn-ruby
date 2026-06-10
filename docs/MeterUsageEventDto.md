# Solifyn::MeterUsageEventDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique usage event ID. |  |
| **meter_id** | **String** | The meter ID this event belongs to. |  |
| **customer_id** | **String** | The customer ID associated with the usage event. |  |
| **value** | **Float** | Numeric usage value recorded for the event. |  |
| **metadata** | **Hash&lt;String, Object&gt;** | Optional event metadata. | [optional] |
| **timestamp** | **Time** | Timestamp when the usage event occurred. |  |
| **processed_at** | **Time** | Timestamp when the usage event was processed. |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::MeterUsageEventDto.new(
  id: evt_9Y3kP4qR7tU1vW2xZ5aB6c,
  meter_id: mtr_8Z1aB2cD3eF4gH5iJ6kL7m,
  customer_id: cus_8n7m6l5k4j3h2g1f0e9d8c,
  value: 1,
  metadata: {plan&#x3D;enterprise, region&#x3D;asia-southeast-1},
  timestamp: 2026-05-23T10:00:00.000Z,
  processed_at: 2026-05-23T10:00:01.000Z
)
```

