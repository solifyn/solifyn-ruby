# Solifyn::MeterIngestResponseDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **processed** | **Float** | Number of successfully processed events. |  |
| **failed** | **Float** | Number of failed events. |  |
| **errors** | **Array&lt;Object&gt;** | List of errors encountered during ingestion. |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::MeterIngestResponseDto.new(
  processed: 5,
  failed: 1,
  errors: [{&quot;event&quot;:&quot;evt_9Y3kP4qR7tU1vW2xZ5aB6c&quot;,&quot;error&quot;:&quot;Meter not found&quot;}]
)
```

