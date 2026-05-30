# Solifyn::UpdateInstanceDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **instance_name** | **String** | The updated friendly name of the instance | [optional] |
| **ip_address** | **String** | The updated IP address of the client device | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::UpdateInstanceDto.new(
  instance_name: Developer Laptop,
  ip_address: 192.168.1.1
)
```

