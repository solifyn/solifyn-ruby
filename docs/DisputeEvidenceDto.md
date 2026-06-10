# Solifyn::DisputeEvidenceDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **cancellation_policy** | **String** | Cancellation policy attachment ID | [optional] |
| **customer_communication** | **String** | Customer communication attachment ID | [optional] |
| **refund_policy** | **String** | Refund policy attachment ID | [optional] |
| **uncategorized** | **String** | Uncategorized attachment ID | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::DisputeEvidenceDto.new(
  cancellation_policy: file_123,
  customer_communication: file_456,
  refund_policy: file_789,
  uncategorized: file_000
)
```

