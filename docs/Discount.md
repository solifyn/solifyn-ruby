# Solifyn::Discount

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique prefix-based identifier of the discount (e.g., &#x60;disc_cs8f67sd7f6fw3fs&#x60;). |  |
| **discount_id** | **String** | Alias for the unique identifier of the discount. |  |
| **code** | **String** | The unique discount code (e.g. SAVE10) used during checkout. |  |
| **name** | **String** | The customer-facing name of the discount code (e.g. Summer Sale). | [optional] |
| **type** | **String** | The discount calculation type: percentage or fixed_amount. |  |
| **amount** | **Integer** | The discount value. For percentage type, it is in basis points (e.g. 1000 &#x3D; 10.00%). For fixed_amount type, it is in cents (e.g. 1000 &#x3D; $10.00). |  |
| **usage_limit** | **Integer** | Maximum number of times this discount code can be redeemed. Null represents unlimited usage. |  |
| **times_used** | **Integer** | The number of times this discount code has been successfully redeemed. |  |
| **expires_at** | **Time** | The expiration timestamp after which the discount code is no longer valid. |  |
| **status** | **String** | The current status of the discount. |  |
| **business_id** | **String** | The unique identifier associated with the business this discount belongs to. |  |
| **created_at** | **Time** | Timestamp indicating exactly when the discount was created. |  |
| **updated_at** | **Time** | Timestamp indicating when the discount was last updated. |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::Discount.new(
  id: disc_cs8f67sd7f6fw3fs,
  discount_id: disc_cs8f67sd7f6fw3fs,
  code: null,
  name: null,
  type: null,
  amount: null,
  usage_limit: null,
  times_used: null,
  expires_at: null,
  status: null,
  business_id: null,
  created_at: null,
  updated_at: null
)
```

