# Solifyn::WebhookPaymentPayload

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Internal payment ID. | [optional] |
| **status** | **String** |  | [optional] |
| **substatus** | **String** |  | [optional] |
| **customer_id** | **String** |  | [optional] |
| **customer_email** | **String** |  | [optional] |
| **customer_name** | **String** |  | [optional] |
| **customer_username** | **String** |  | [optional] |
| **product_title** | **String** |  | [optional] |
| **product_route** | **String** |  | [optional] |
| **plan_id** | **String** |  | [optional] |
| **membership_id** | **String** |  | [optional] |
| **membership_status** | **String** |  | [optional] |
| **billing_reason** | **String** |  | [optional] |
| **amount** | **String** | Dollar value, 2 d.p. | [optional] |
| **subtotal** | **String** |  | [optional] |
| **usd_total** | **String** |  | [optional] |
| **fee_amount** | **String** |  | [optional] |
| **amount_after_fees** | **String** |  | [optional] |
| **tax_amount** | **String** |  | [optional] |
| **tax_behavior** | **String** |  | [optional] |
| **tax_refunded_amount** | **String** |  | [optional] |
| **refunded_amount** | **String** |  | [optional] |
| **settlement_amount** | **String** |  | [optional] |
| **settlement_currency** | **String** |  | [optional] |
| **settlement_exchange_rate** | **String** |  | [optional] |
| **currency** | **String** |  | [optional] |
| **refundable** | **Boolean** |  | [optional] |
| **retryable** | **Boolean** |  | [optional] |
| **auto_refunded** | **Boolean** |  | [optional] |
| **payment_method** | **String** |  | [optional] |
| **card_brand** | **String** |  | [optional] |
| **card_last4** | **String** |  | [optional] |
| **card_exp_month** | **Integer** |  | [optional] |
| **card_exp_year** | **Integer** |  | [optional] |
| **billing_address** | [**WebhookPaymentPayloadBillingAddress**](WebhookPaymentPayloadBillingAddress.md) |  | [optional] |
| **license_key** | **String** |  | [optional] |
| **files_snapshot** | **Array&lt;Object&gt;** |  | [optional] |
| **checkout_id** | **String** |  | [optional] |
| **discount_code** | **String** |  | [optional] |
| **failure_message** | **String** |  | [optional] |
| **paid_at** | **Time** |  | [optional] |
| **refunded_at** | **Time** |  | [optional] |
| **dispute_alerted_at** | **Time** |  | [optional] |
| **last_payment_attempt** | **Time** |  | [optional] |
| **next_payment_attempt** | **Time** |  | [optional] |
| **created_at** | **Time** |  | [optional] |
| **updated_at** | **Time** |  | [optional] |
| **payment_event_type** | **String** |  | [optional] |
| **last_event_type** | **String** |  | [optional] |
| **business_id** | **String** |  | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::WebhookPaymentPayload.new(
  id: pay_019e60cb...,
  status: created,
  substatus: incomplete,
  customer_id: null,
  customer_email: null,
  customer_name: null,
  customer_username: null,
  product_title: null,
  product_route: null,
  plan_id: null,
  membership_id: null,
  membership_status: null,
  billing_reason: subscription_create,
  amount: 100.00,
  subtotal: 100.00,
  usd_total: 100.00,
  fee_amount: 3.25,
  amount_after_fees: 96.75,
  tax_amount: null,
  tax_behavior: null,
  tax_refunded_amount: null,
  refunded_amount: 0,
  settlement_amount: null,
  settlement_currency: null,
  settlement_exchange_rate: null,
  currency: USD,
  refundable: null,
  retryable: null,
  auto_refunded: null,
  payment_method: card,
  card_brand: visa,
  card_last4: 4242,
  card_exp_month: null,
  card_exp_year: null,
  billing_address: null,
  license_key: null,
  files_snapshot: null,
  checkout_id: null,
  discount_code: null,
  failure_message: null,
  paid_at: null,
  refunded_at: null,
  dispute_alerted_at: null,
  last_payment_attempt: null,
  next_payment_attempt: null,
  created_at: null,
  updated_at: null,
  payment_event_type: null,
  last_event_type: null,
  business_id: null
)
```

