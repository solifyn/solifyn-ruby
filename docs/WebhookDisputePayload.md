# Solifyn::WebhookDisputePayload

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Internal dispute ID. | [optional] |
| **payment_id** | **String** |  | [optional] |
| **amount** | **String** | Dollar value, 2 d.p. | [optional] |
| **currency** | **String** |  | [optional] |
| **status** | **String** |  | [optional] |
| **reason** | **String** |  | [optional] |
| **editable** | **Boolean** |  | [optional] |
| **needs_response_by** | **Time** |  | [optional] |
| **customer_name** | **String** |  | [optional] |
| **customer_email** | **String** |  | [optional] |
| **notes** | **String** |  | [optional] |
| **created_at** | **Time** |  | [optional] |
| **updated_at** | **Time** |  | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::WebhookDisputePayload.new(
  id: dsp_abc123,
  payment_id: pay_019e60cb...,
  amount: 100.00,
  currency: USD,
  status: needs_response,
  reason: fraudulent,
  editable: null,
  needs_response_by: null,
  customer_name: null,
  customer_email: null,
  notes: null,
  created_at: null,
  updated_at: null
)
```

