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
  headers: {&quot;X-Example&quot;:&quot;123&quot;,&quot;X-Foobar&quot;:&quot;Bar&quot;},
  sensitive: [&quot;Authorization&quot;]
)
```

