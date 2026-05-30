# Solifyn::SubscriptionAction

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_days** | **Float** | Number of free days to add (used with action: add_free_days) | [optional] |
| **cancellation_mode** | **String** | Cancellation mode (used with action: cancel) | [optional] |
| **void_payments** | **Boolean** | Whether to void subsequent payments (used with action: pause) | [optional] |
| **addon_product_id** | **String** | ID of the addon product to adjust seats for (used with action: adjust_seats) | [optional] |
| **new_quantity** | **Float** | The new seat quantity (used with action: adjust_seats) | [optional] |
| **proration_type** | **String** | Proration strategy mode (used with action: adjust_seats) | [optional] |
| **idempotency_key** | **String** | A unique idempotency key to prevent duplicate mutative actions for network transient retries. | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::SubscriptionAction.new(
  free_days: 30,
  cancellation_mode: immediate,
  void_payments: true,
  addon_product_id: prod_seat_123,
  new_quantity: 5,
  proration_type: do_not_bill,
  idempotency_key: sub_action_idem_123
)
```

