# Solifyn::SubscriptionDetail

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **subscription** | [**Subscription**](Subscription.md) | The main subscription details |  |
| **payments** | [**Array&lt;Order&gt;**](Order.md) | The subscription payments / invoice billing history |  |
| **purchased_addons** | [**Array&lt;ResolvedAddon&gt;**](ResolvedAddon.md) | List of purchased addons associated with this subscription |  |
| **product** | [**SubscriptionDetailProduct**](SubscriptionDetailProduct.md) | The core product information associated with this subscription |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::SubscriptionDetail.new(
  subscription: null,
  payments: null,
  purchased_addons: null,
  product: null
)
```

