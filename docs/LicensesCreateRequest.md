# Solifyn::LicensesCreateRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **String** | The unique product identifier (internal product ID or ID) for which the license key will be issued. |  |
| **customer_id** | **String** | The unique customer identifier (internal customer ID or ID) who will own this license key. |  |
| **activation_limit** | **Integer** | The maximum number of concurrent device or server activations allowed for this license key. | [optional] |
| **expiry_hours** | **Integer** | Relative validity period of the license in hours starting from the time of creation. | [optional] |
| **key** | **String** | Optional custom license key string. If not provided, a random uppercase cryptographic serial key (e.g., ABCD-EFGH) will be generated automatically. | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::LicensesCreateRequest.new(
  product_id: null,
  customer_id: null,
  activation_limit: null,
  expiry_hours: null,
  key: null
)
```

