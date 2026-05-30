# Solifyn::LicensesActivateRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **key** | **String** | The license key. |  |
| **device_identifier** | **String** | Unique identifier of the device/machine being activated. |  |
| **name** | **String** | A user-friendly label/name for the instance. |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::LicensesActivateRequest.new(
  key: null,
  device_identifier: null,
  name: null
)
```

