# Solifyn::UpdateCollectionDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | The friendly name of the collection | [optional] |
| **description** | **String** | A detailed description of this collection | [optional] |
| **image_url** | **String** | The display cover image URL for this collection | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::UpdateCollectionDto.new(
  name: Winter Course Bundle,
  description: Get all our premium programming courses at a highly discounted price.,
  image_url: https://images.unsplash.com/photo-123
)
```

