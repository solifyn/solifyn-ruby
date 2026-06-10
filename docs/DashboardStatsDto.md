# Solifyn::DashboardStatsDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **revenue** | **Float** | Gross revenue in cents |  |
| **orders_count** | **Float** | Total payments processed count |  |
| **refunds_count** | **Float** | Gross amount refunded in cents |  |
| **active_memberships** | **Float** | Number of active paying customers/memberships |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::DashboardStatsDto.new(
  revenue: 500000,
  orders_count: 120,
  refunds_count: 1500,
  active_memberships: 85
)
```

