# Solifyn::CollectionDetailResponseDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The collection ID |  |
| **name** | **String** | The name of the collection |  |
| **description** | **String** | A brief description of the collection | [optional] |
| **image_url** | **String** | URL of the collection image | [optional] |
| **status** | **String** | Status of the collection |  |
| **business_id** | **String** | The unique identifier of the business owning this collection. |  |
| **is_permanently_deleted** | **Boolean** | Indicates if the collection has been permanently deleted. |  |
| **created_at** | **Time** | Timestamp when the collection was created |  |
| **updated_at** | **Time** | Timestamp when the collection was last updated |  |
| **products** | [**Array&lt;CollectionProductDto&gt;**](CollectionProductDto.md) | Full product details including quantity for each item in the collection | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::CollectionDetailResponseDto.new(
  id: null,
  name: Summer Bundle,
  description: Everything you need for summer.,
  image_url: https://example.com/image.png,
  status: ACTIVE,
  business_id: biz_4r5t6y7u8i9o,
  is_permanently_deleted: false,
  created_at: 2025-01-01T12:00Z,
  updated_at: 2025-01-01T12:00Z,
  products: null
)
```

