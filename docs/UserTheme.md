# Solifyn::UserTheme

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Theme configuration ID |  |
| **config** | **Object** | Styling config JSON (fontFamily, borderRadius, colors) |  |
| **avatar_url** | **String** | Logo/avatar image URL | [optional] |
| **banner_url** | **String** | Header banner image URL | [optional] |
| **business_id** | **String** | The linked business ID |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::UserTheme.new(
  id: theme_123,
  config: {&quot;theme&quot;:{&quot;primaryColor&quot;:&quot;#0f172a&quot;,&quot;fontFamily&quot;:&quot;Inter&quot;}},
  avatar_url: https://acme.com/avatar.png,
  banner_url: https://acme.com/banner.png,
  business_id: biz_123
)
```

