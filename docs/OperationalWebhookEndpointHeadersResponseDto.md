# Solifyn::OperationalWebhookEndpointHeadersResponseDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **headers** | **Object** | Key-value headers sent with the webhook. |  |
| **sensitive** | **Array&lt;String&gt;** | List of sensitive header keys (e.g. Authorization) that are masked. |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::OperationalWebhookEndpointHeadersResponseDto.new(
  headers: {X-Example&#x3D;123, X-Foobar&#x3D;Bar},
  sensitive: [Authorization]
)
```

