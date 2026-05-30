# Solifyn::UserStats

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **summary** | [**DashboardStatsDto**](DashboardStatsDto.md) | Core metric summaries |  |
| **chart_data** | **Array&lt;Object&gt;** | Graph data plotting daily analytics over past month |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::UserStats.new(
  summary: null,
  chart_data: [{&quot;date&quot;:&quot;2025-01-01&quot;,&quot;revenue&quot;:12000,&quot;orders&quot;:3}]
)
```

