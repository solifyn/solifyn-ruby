# Solifyn::DisputeEvidenceUpdate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **cancellation_policy_attachment** | [**DisputeAttachmentDto**](DisputeAttachmentDto.md) | Evidence showing cancellation policy details | [optional] |
| **customer_communication_attachment** | [**DisputeAttachmentDto**](DisputeAttachmentDto.md) | Evidence demonstrating communications with the customer | [optional] |
| **refund_policy_attachment** | [**DisputeAttachmentDto**](DisputeAttachmentDto.md) | Evidence showing refund policy details | [optional] |
| **uncategorized_attachment** | [**DisputeAttachmentDto**](DisputeAttachmentDto.md) | Uncategorized supporting files or documents | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::DisputeEvidenceUpdate.new(
  cancellation_policy_attachment: null,
  customer_communication_attachment: null,
  refund_policy_attachment: null,
  uncategorized_attachment: null
)
```

