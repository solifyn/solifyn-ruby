# Solifyn::Invoice

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Unique invoice identifier. |  |
| **order_id** | **String** | Associated order ID. |  |
| **url** | **String** | Invoice URL for downloading or viewing PDF. |  |
| **status** | **String** | Status of invoice. |  |
| **created_at** | **Time** | Invoice creation date. |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::Invoice.new(
  id: inv_123,
  order_id: pay_123,
  url: https://api.solifyn.com/v1/orders/pay_123/invoice/pdf,
  status: paid,
  created_at: 2026-05-22T08:00:00Z
)
```

