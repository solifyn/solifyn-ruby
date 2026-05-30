# Solifyn::SubscriptionSeatAdjustment

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **success** | **Boolean** | Indicates if the seat adjustment was successful |  |
| **subscription_id** | **String** | The customer subscription ID |  |
| **addon_product_id** | **String** | The unique ID of the addon product |  |
| **old_quantity** | **Float** | The previous seat quantity |  |
| **new_quantity** | **Float** | The new seat quantity after adjustment |  |
| **quantity_delta** | **Float** | The difference in seat quantity |  |
| **proration_type** | **String** | The proration strategy type applied |  |
| **cost_impact** | **Float** | Calculated pro-rata price cost impact in currency unit (charged or credited) |  |
| **currency** | **String** | Billing currency |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::SubscriptionSeatAdjustment.new(
  success: true,
  subscription_id: mem_123,
  addon_product_id: prod_seat_123,
  old_quantity: 2,
  new_quantity: 5,
  quantity_delta: 3,
  proration_type: do_not_bill,
  cost_impact: 0,
  currency: usd
)
```

