# Solifyn::UserThemeUpdate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **config** | **Object** | JSON object specifying styling parameters (colors, fonts, borders) | [optional] |
| **avatar_url** | **String** | URL of the store avatar/logo | [optional] |
| **banner_url** | **String** | URL of the store banner header image | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::UserThemeUpdate.new(
  config: {&quot;theme&quot;:{&quot;primaryColor&quot;:&quot;#0f172a&quot;,&quot;fontFamily&quot;:&quot;Inter&quot;}},
  avatar_url: https://acme.com/avatar.png,
  banner_url: https://acme.com/banner.png
)
```

