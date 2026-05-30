# Solifyn::Business

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique business ID |  |
| **title** | **String** | Title or name of the business |  |
| **description** | **String** | A description explaining what the business does | [optional] |
| **whop_id** | **String** | The Whop Company ID |  |
| **merchant_id** | **String** | The merchant owner ID |  |
| **verified** | **Boolean** | Whether the business has been KYC-verified on Whop |  |
| **send_customer_emails** | **Boolean** | Whether auto-emails are enabled for customers |  |
| **member_count** | **Float** | Total members/customers under this business |  |
| **route** | **String** | Whop friendly URL path route | [optional] |
| **default_currency** | **String** | The default currency of the business |  |
| **published_reviews_count** | **Float** | Number of published user reviews on Whop |  |
| **metadata** | **Object** | Custom key-value metadata | [optional] |
| **target_audience** | **String** | The target audience description | [optional] |
| **social_links** | **Object** | Social links setup | [optional] |
| **affiliate_instructions** | **String** | Markdown instructions for affiliates | [optional] |
| **whop_created_at** | **Time** | Whop account creation timestamp | [optional] |
| **whop_updated_at** | **Time** | Whop account last updated timestamp | [optional] |
| **created_at** | **Time** | Timestamp when the business record was created |  |
| **updated_at** | **Time** | Timestamp when the business record was last updated |  |
| **logo_url** | **String** | Brand logo image URL resolved from primary brand | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::Business.new(
  id: biz_123,
  title: Acme Inc,
  description: Premium tools and subscriptions,
  whop_id: comp_123,
  merchant_id: mer_123,
  verified: true,
  send_customer_emails: true,
  member_count: 100,
  route: acme,
  default_currency: USD,
  published_reviews_count: 15,
  metadata: null,
  target_audience: Developers and creators,
  social_links: null,
  affiliate_instructions: Promote our tools and earn 30% commission.,
  whop_created_at: 2025-01-01T12:00:00Z,
  whop_updated_at: 2025-01-01T12:00:00Z,
  created_at: 2025-01-01T12:00:00Z,
  updated_at: 2025-01-01T12:00:00Z,
  logo_url: https://acme.com/logo.png
)
```

