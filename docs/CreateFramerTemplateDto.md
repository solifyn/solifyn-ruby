# Solifyn::CreateFramerTemplateDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | The name of the Framer template. |  |
| **remix_link** | **String** | The public Framer remix link. |  |
| **description** | **String** | A brief description of the template. | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::CreateFramerTemplateDto.new(
  name: Portfolio Template,
  remix_link: https://framer.com/projects/xyz,
  description: Premium dark-mode portfolio.
)
```

