# Solifyn::BusinessFullCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **title** | **String** | The title/name of the business |  |
| **website_url** | **String** | The primary website URL for the business | [optional] |
| **country** | **String** | Country name of the business registration |  |
| **category** | **String** | The business market category (e.g. software, media) | [optional] |
| **referred_by_code** | **String** | Optional partner referral code used during signup | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::BusinessFullCreate.new(
  title: Acme LLC,
  website_url: https://acme.com,
  country: Vietnam,
  category: software,
  referred_by_code: partner_abc123
)
```

