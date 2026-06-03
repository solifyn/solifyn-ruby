# Solifyn::WebhookSubscriptionPayload

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The subscription ID. | [optional] |
| **status** | **String** | Current status of the subscription. | [optional] |
| **cancel_at_period_end** | **Boolean** |  | [optional] |
| **renewal_period_start** | **Time** |  | [optional] |
| **renewal_period_end** | **Time** |  | [optional] |
| **currency** | **String** |  | [optional] |
| **amount** | **Float** |  | [optional] |
| **customer_id** | **String** |  | [optional] |
| **customer_email** | **String** |  | [optional] |
| **customer_name** | **String** |  | [optional] |
| **product_id** | **String** |  | [optional] |
| **product_title** | **String** |  | [optional] |
| **created_at** | **Time** |  | [optional] |
| **updated_at** | **Time** |  | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::WebhookSubscriptionPayload.new(
  id: null,
  status: null,
  cancel_at_period_end: null,
  renewal_period_start: null,
  renewal_period_end: null,
  currency: null,
  amount: null,
  customer_id: null,
  customer_email: null,
  customer_name: null,
  product_id: null,
  product_title: null,
  created_at: null,
  updated_at: null
)
```

