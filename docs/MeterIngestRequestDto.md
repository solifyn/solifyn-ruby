# Solifyn::MeterIngestRequestDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **events** | [**Array&lt;MeterIngestEventDto&gt;**](MeterIngestEventDto.md) | List of usage events to ingest. |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::MeterIngestRequestDto.new(
  events: null
)
```

