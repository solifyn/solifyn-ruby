# Solifyn::CreateCollectionDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | The friendly name of the collection |  |
| **description** | **String** | A detailed description of this collection | [optional] |
| **image_url** | **String** | The display cover image URL for this collection | [optional] |
| **status** | **String** | The collection status | [optional] |
| **products** | [**Array&lt;CollectionProductEntry&gt;**](CollectionProductEntry.md) | List of products to include in this collection. At least one product is required. |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::CreateCollectionDto.new(
  name: Winter Course Bundle,
  description: Get all our premium programming courses at a highly discounted price.,
  image_url: https://images.unsplash.com/photo-123,
  status: ACTIVE,
  products: null
)
```

