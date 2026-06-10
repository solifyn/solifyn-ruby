# Solifyn::SupportedCurrenciesResponseDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **label** | **String** | The label display name of the currency |  |
| **value** | **String** | The currency code |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::SupportedCurrenciesResponseDto.new(
  label: US Dollar,
  value: usd
)
```

