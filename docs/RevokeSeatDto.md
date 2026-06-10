# Solifyn::RevokeSeatDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **String** | The product ID of the addon (Whop Product ID or local ID). |  |
| **quantity** | **Integer** | The number of seats to revoke/deduct. |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::RevokeSeatDto.new(
  product_id: prod_lBrPxQcGN8dBM,
  quantity: 1
)
```

