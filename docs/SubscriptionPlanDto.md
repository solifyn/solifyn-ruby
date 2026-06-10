# Solifyn::SubscriptionPlanDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique ID of the plan |  |
| **metadata** | **Object** | Additional metadata associated with the plan | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::SubscriptionPlanDto.new(
  id: plan_123,
  metadata: {}
)
```

