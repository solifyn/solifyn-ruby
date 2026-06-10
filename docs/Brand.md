# Solifyn::Brand

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique brand ID |  |
| **name** | **String** | The brand name |  |
| **website_url** | **String** | The website URL associated with the brand | [optional] |
| **support_email** | **String** | Support email address for customer service | [optional] |
| **description** | **String** | Short description of the brand | [optional] |
| **logo_url** | **String** | Brand logo image URL | [optional] |
| **is_primary** | **Boolean** | Whether this is the primary brand for the merchant business |  |
| **statement_descriptor** | **String** | Credit card statement descriptor | [optional] |
| **merchant_id** | **String** | The merchant ID owning the brand |  |
| **business_id** | **String** | The business ID linked to the brand | [optional] |
| **created_at** | **Time** | Timestamp when the brand was created |  |
| **updated_at** | **Time** | Timestamp when the brand was last updated |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::Brand.new(
  id: brd_123,
  name: Acme Corp,
  website_url: https://acme.com,
  support_email: support@acme.com,
  description: A leading provider of ACME tools.,
  logo_url: https://acme.com/logo.png,
  is_primary: true,
  statement_descriptor: ACME CORP INC,
  merchant_id: mer_123,
  business_id: biz_123,
  created_at: 2025-01-01T12:00Z,
  updated_at: 2025-01-01T12:00Z
)
```

