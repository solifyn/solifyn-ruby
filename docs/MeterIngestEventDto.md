# Solifyn::MeterIngestEventDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **event_id** | **String** | Unique usage event ID for idempotency. |  |
| **customer_id** | **String** | Unique customer ID associated with the event. |  |
| **event_name** | **String** | Event name that should match a meter eventName. |  |
| **value** | **Float** | Event quantity value. | [optional][default to 1] |
| **metadata** | **Hash&lt;String, Object&gt;** | Metadata attached to the usage event. | [optional] |
| **timestamp** | **String** | Timestamp of the event in ISO 8601 format. | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::MeterIngestEventDto.new(
  event_id: evt_9Y3kP4qR7tU1vW2xZ5aB6c,
  customer_id: cus_8n7m6l5k4j3h2g1f0e9d8c,
  event_name: api.request,
  value: 1,
  metadata: {&quot;plan&quot;:&quot;enterprise&quot;,&quot;region&quot;:&quot;asia-southeast-1&quot;},
  timestamp: 2026-05-23T10:00:00.000Z
)
```

