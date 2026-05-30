# Solifyn::BrandUpdate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Name of the brand | [optional] |
| **website_url** | **String** | The website URL associated with the brand | [optional] |
| **support_email** | **String** | Support email address for customer service | [optional] |
| **description** | **String** | Short description of the brand | [optional] |
| **logo_url** | **String** | Brand logo image URL | [optional] |
| **statement_descriptor** | **String** | Credit card statement descriptor (Max 22 chars) | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::BrandUpdate.new(
  name: Acme Corp,
  website_url: https://acme.com,
  support_email: support@acme.com,
  description: A leading provider of ACME tools.,
  logo_url: https://acme.com/logo.png,
  statement_descriptor: ACME CORP INC
)
```

