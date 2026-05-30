# Solifyn::DiscountCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **code** | **String** | Unique discount code string (will be automatically capitalized). |  |
| **name** | **String** | Customer-facing name of the discount. | [optional] |
| **type** | **String** | Calculation type: percentage or fixed_amount. |  |
| **amount** | **Float** | The discount value. If percentage, enter value like 10 for 10%. If fixed_amount, enter value like 10 for $10.00. |  |
| **usage_limit** | **Integer** | Maximum number of redemptions allowed. | [optional] |
| **expires_at** | **Time** | Expiration timestamp for the discount. | [optional] |
| **subscription_cycles** | **Integer** | Number of subscription cycles this discount applies to. | [optional] |
| **restricted_to** | **Array&lt;String&gt;** | List of product IDs this discount is restricted to. | [optional] |
| **preserve_on_plan_change** | **Boolean** | Whether to preserve the discount when subscription plan changes. | [optional] |
| **metadata** | **Object** | Custom metadata for the discount. | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::DiscountCreate.new(
  code: null,
  name: null,
  type: null,
  amount: null,
  usage_limit: null,
  expires_at: null,
  subscription_cycles: null,
  restricted_to: null,
  preserve_on_plan_change: null,
  metadata: null
)
```

