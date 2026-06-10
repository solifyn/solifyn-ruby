# Solifyn::WebhookEntitlementGrantPayload

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique entitlement grant ID. | [optional] |
| **business_id** | **String** | The business ID context. | [optional] |
| **customer_id** | **String** | The customer ID. | [optional] |
| **payment_id** | **String** | Associated payment transaction ID. | [optional] |
| **product_id** | **String** | The purchased product ID. | [optional] |
| **type** | **String** | The type of entitlement (e.g. GITHUB). | [optional] |
| **github_repo** | **String** | Target GitHub repository (owner/repo) if type is GITHUB. | [optional] |
| **github_permission** | **String** | GitHub access permission level if type is GITHUB. | [optional] |
| **github_username** | **String** | The connected customer GitHub username. | [optional] |
| **status** | **String** | Delivery status of the collaborator invite (PENDING, DELIVERED, FAILED, REVOKED). | [optional] |
| **oauth_url** | **String** | OAuth URL to redirect the customer to. | [optional] |
| **error_details** | **String** | Error message if invitation delivery failed. | [optional] |
| **created_at** | **Time** |  | [optional] |
| **updated_at** | **Time** |  | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::WebhookEntitlementGrantPayload.new(
  id: grant_123456,
  business_id: biz_123456,
  customer_id: cust_123456,
  payment_id: pay_123456,
  product_id: prod_123456,
  type: GITHUB,
  github_repo: solifyn/premium-app,
  github_permission: pull,
  github_username: octocat,
  status: PENDING,
  oauth_url: https://github.com/login/oauth/authorize...,
  error_details: Permission denied,
  created_at: null,
  updated_at: null
)
```

