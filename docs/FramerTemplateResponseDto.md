# Solifyn::FramerTemplateResponseDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique Framer template ID. |  |
| **business_id** | **String** | The business ID owning the template. |  |
| **name** | **String** | The name of the Framer template. |  |
| **remix_link** | **String** | The public Framer remix link. |  |
| **description** | **String** | A brief description of the template. | [optional] |
| **created_at** | **String** | Creation timestamp. |  |
| **updated_at** | **String** | Modification timestamp. |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::FramerTemplateResponseDto.new(
  id: tmpl_123456,
  business_id: biz_123456,
  name: Portfolio Template,
  remix_link: https://framer.com/projects/xyz,
  description: Premium dark-mode portfolio.,
  created_at: null,
  updated_at: null
)
```

