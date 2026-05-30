# Solifyn::UserPage

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Store page record ID |  |
| **subdomain** | **String** | Unique subdomain |  |
| **store_name** | **String** | Friendly store name |  |
| **config** | **Object** | Styling config JSON |  |
| **business_id** | **String** | Linked business ID |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::UserPage.new(
  id: page_123,
  subdomain: acme,
  store_name: Acme Shop,
  config: {&quot;theme&quot;:{&quot;primaryColor&quot;:&quot;#0f172a&quot;}},
  business_id: biz_123
)
```

