# Solifyn::Order

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Unique internal database identifier. |  |
| **invoice_url** | **String** | The invoice print URL. |  |
| **customer** | [**OrderCustomer**](OrderCustomer.md) | Customer details. |  |
| **total_amount** | **Integer** | Total paid amount in cents. |  |
| **subtotal** | **Integer** | Subtotal amount in cents. |  |
| **usd_total** | **Float** | Total paid amount converted to USD. | [optional] |
| **tax_amount** | **Integer** | Tax amount in cents. |  |
| **application_fee** | **Integer** | Application fee in cents. |  |
| **amount_after_fees** | **Integer** | Net amount after fees in cents. |  |
| **currency** | **String** | Currency code. |  |
| **status** | **String** | Current status of the payment. |  |
| **created_at** | **Time** | Payment creation timestamp. |  |
| **paid_at** | **Time** | Payment completion/paid timestamp. | [optional] |
| **payment_method** | **String** | Payment method utilized. |  |
| **card_last_four** | **String** | Last four digits of card used. | [optional] |
| **card_network** | **String** | Card network/brand. | [optional] |
| **card_type** | **String** | Card type. | [optional] |
| **billing** | [**OrderBilling**](OrderBilling.md) | Billing address details. | [optional] |
| **product_cart** | [**Array&lt;OrderProductCart&gt;**](OrderProductCart.md) | Products purchased in this order. |  |
| **metadata** | **Object** | Custom metadata payload associated with this payment. | [optional] |
| **order** | [**OrderDetail**](OrderDetail.md) | Order details snapshot. | [optional] |
| **refundable** | **Boolean** | Indicates whether the order is eligible for refund. |  |
| **refunds** | [**Array&lt;OrderRefund&gt;**](OrderRefund.md) | List of refunds associated with this payment. | [optional] |
| **business_id** | **String** | Business unique ID identifier. |  |
| **business_name** | **String** | Business display title/name. |  |
| **billing_reason** | **String** | Billing reason detail. | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::Order.new(
  id: pay_123,
  invoice_url: https://solifyn.com/transactions/payments/pay_123/print,
  customer: null,
  total_amount: 2900,
  subtotal: 2900,
  usd_total: 30.6,
  tax_amount: 0,
  application_fee: 150,
  amount_after_fees: 2750,
  currency: usd,
  status: paid,
  created_at: 2026-05-22T08:00Z,
  paid_at: 2026-05-22T08:05Z,
  payment_method: card,
  card_last_four: 4242,
  card_network: visa,
  card_type: visa,
  billing: null,
  product_cart: null,
  metadata: null,
  order: null,
  refundable: true,
  refunds: null,
  business_id: biz_123,
  business_name: Acme SaaS Corp,
  billing_reason: subscription_cycle
)
```

