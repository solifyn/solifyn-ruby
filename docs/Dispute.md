# Solifyn::Dispute

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The dispute ID |  |
| **whop_id** | **String** | The Whop Dispute ID |  |
| **amount** | **Float** | The dispute amount |  |
| **currency** | **String** | The currency code |  |
| **status** | **String** | The status of the dispute |  |
| **reason** | **String** | The reason for the dispute | [optional] |
| **editable** | **Boolean** | Whether the evidence is still editable |  |
| **needs_response_by** | **Time** | Timestamp by when evidence must be submitted | [optional] |
| **visa_rdr** | **Boolean** | Whether Visa RDR was applied |  |
| **billing_address** | **String** | Customer billing address details | [optional] |
| **customer_name** | **String** | Customer name | [optional] |
| **customer_email** | **String** | Customer email address | [optional] |
| **notes** | **String** | Additional notes | [optional] |
| **product_description** | **String** | Product or service description | [optional] |
| **service_date** | **String** | Service or purchase date | [optional] |
| **access_activity_log** | **String** | Log of access activity | [optional] |
| **evidence** | [**DisputeEvidenceDto**](DisputeEvidenceDto.md) | Evidence attachments associated with the dispute | [optional] |
| **payment_id** | **String** | The associated payment ID |  |
| **business_id** | **String** | The associated business ID |  |
| **created_at** | **Time** | Timestamp when the dispute was created |  |
| **updated_at** | **Time** | Timestamp when the dispute was last updated |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::Dispute.new(
  id: dsp_123,
  whop_id: dspt_123,
  amount: 15,
  currency: usd,
  status: warning_needs_response,
  reason: Product not received,
  editable: true,
  needs_response_by: 2025-01-01T12:00Z,
  visa_rdr: false,
  billing_address: 123 Main St, New York, NY,
  customer_name: John Doe,
  customer_email: customer@example.com,
  notes: Customer requested a refund,
  product_description: Premium Subscription,
  service_date: 2025-01-01,
  access_activity_log: Logged in from IP 1.2.3.4,
  evidence: null,
  payment_id: pay_123,
  business_id: biz_123,
  created_at: 2025-01-01T12:00Z,
  updated_at: 2025-01-01T12:00Z
)
```

