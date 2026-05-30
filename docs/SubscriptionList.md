# Solifyn::SubscriptionList

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **items** | [**Array&lt;Subscription&gt;**](Subscription.md) | List of customer subscriptions |  |
| **total_count** | **Float** | Total count of subscriptions matching the filters |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::SubscriptionList.new(
  items: null,
  total_count: 1
)
```

