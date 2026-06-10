# Solifyn::LicensesUpdateInstancePostRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **instance_name** | **String** | A new human-readable display name for this instance. | [optional] |
| **ip_address** | **String** | A new IP address to record for this instance. | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::LicensesUpdateInstancePostRequest.new(
  instance_name: MacBook Pro 16&quot;,
  ip_address: 203.0.113.42
)
```

