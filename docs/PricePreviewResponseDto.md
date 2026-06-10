# Solifyn::PricePreviewResponseDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **original_price** | **Float** | Original price of the product after discounts |  |
| **original_currency** | **String** | Original ISO currency code of the product |  |
| **converted_price** | **Float** | Converted price of the product |  |
| **converted_currency** | **String** | Converted ISO currency code of the product |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::PricePreviewResponseDto.new(
  original_price: 10,
  original_currency: USD,
  converted_price: 250000,
  converted_currency: VND
)
```

