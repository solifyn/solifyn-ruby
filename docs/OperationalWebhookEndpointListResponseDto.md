# Solifyn::OperationalWebhookEndpointListResponseDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**Array&lt;OperationalWebhookEndpointResponseDto&gt;**](OperationalWebhookEndpointResponseDto.md) |  |  |
| **done** | **Boolean** |  |  |
| **iterator** | **Object** |  | [optional] |
| **prev_iterator** | **Object** |  | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::OperationalWebhookEndpointListResponseDto.new(
  data: null,
  done: true,
  iterator: iterator-token-abc,
  prev_iterator: prev-iterator-token-abc
)
```

