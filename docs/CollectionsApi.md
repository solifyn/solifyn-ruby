# Solifyn::CollectionsApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**collections_add_products**](CollectionsApi.md#collections_add_products) | **POST** /v1/collections/{id}/products | Add Products to Collection |
| [**collections_archive**](CollectionsApi.md#collections_archive) | **DELETE** /v1/collections/{id} | Archive Collection |
| [**collections_create**](CollectionsApi.md#collections_create) | **POST** /v1/collections | Create Collection |
| [**collections_delete_product**](CollectionsApi.md#collections_delete_product) | **DELETE** /v1/collections/{id}/products/{productId} | Remove Product from Collection |
| [**collections_get**](CollectionsApi.md#collections_get) | **GET** /v1/collections/{id} | Retrieve Collection |
| [**collections_list**](CollectionsApi.md#collections_list) | **GET** /v1/collections | List Collections |
| [**collections_list_archived**](CollectionsApi.md#collections_list_archived) | **GET** /v1/collections/archived | List Archived Collections |
| [**collections_unarchive**](CollectionsApi.md#collections_unarchive) | **POST** /v1/collections/{id}/unarchive | Unarchive Collection |
| [**collections_update**](CollectionsApi.md#collections_update) | **PATCH** /v1/collections/{id} | Update Collection |
| [**collections_update_product**](CollectionsApi.md#collections_update_product) | **PATCH** /v1/collections/{id}/products/{productId} | Update Collection Product |


## collections_add_products

> <CollectionResponseDto> collections_add_products(id, add_collection_products_dto)

Add Products to Collection

Add one or more products to a collection. If a product already exists, its quantity is updated.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::CollectionsApi.new
id = 'col_123' # String | Collection ID
add_collection_products_dto = Solifyn::AddCollectionProductsDto.new({products: [Solifyn::CollectionProductEntry.new({id: 'prod_123', quantity: 1})]}) # AddCollectionProductsDto | 

begin
  # Add Products to Collection
  result = api_instance.collections_add_products(id, add_collection_products_dto)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling CollectionsApi->collections_add_products: #{e}"
end
```

#### Using the collections_add_products_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CollectionResponseDto>, Integer, Hash)> collections_add_products_with_http_info(id, add_collection_products_dto)

```ruby
begin
  # Add Products to Collection
  data, status_code, headers = api_instance.collections_add_products_with_http_info(id, add_collection_products_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CollectionResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling CollectionsApi->collections_add_products_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Collection ID |  |
| **add_collection_products_dto** | [**AddCollectionProductsDto**](AddCollectionProductsDto.md) |  |  |

### Return type

[**CollectionResponseDto**](CollectionResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## collections_archive

> <CollectionArchivedResponseDto> collections_archive(id)

Archive Collection

Deactivate and move a collection to archives.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::CollectionsApi.new
id = 'col_123' # String | Collection ID

begin
  # Archive Collection
  result = api_instance.collections_archive(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling CollectionsApi->collections_archive: #{e}"
end
```

#### Using the collections_archive_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CollectionArchivedResponseDto>, Integer, Hash)> collections_archive_with_http_info(id)

```ruby
begin
  # Archive Collection
  data, status_code, headers = api_instance.collections_archive_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CollectionArchivedResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling CollectionsApi->collections_archive_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Collection ID |  |

### Return type

[**CollectionArchivedResponseDto**](CollectionArchivedResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## collections_create

> <CollectionResponseDto> collections_create(create_collection_dto)

Create Collection

Generate a new product collection for checkout packaging.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::CollectionsApi.new
create_collection_dto = Solifyn::CreateCollectionDto.new({name: 'Winter Course Bundle', products: [Solifyn::CollectionProductEntry.new({id: 'prod_123', quantity: 1})]}) # CreateCollectionDto | 

begin
  # Create Collection
  result = api_instance.collections_create(create_collection_dto)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling CollectionsApi->collections_create: #{e}"
end
```

#### Using the collections_create_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CollectionResponseDto>, Integer, Hash)> collections_create_with_http_info(create_collection_dto)

```ruby
begin
  # Create Collection
  data, status_code, headers = api_instance.collections_create_with_http_info(create_collection_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CollectionResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling CollectionsApi->collections_create_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_collection_dto** | [**CreateCollectionDto**](CreateCollectionDto.md) |  |  |

### Return type

[**CollectionResponseDto**](CollectionResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## collections_delete_product

> <CollectionProductDeletedResponseDto> collections_delete_product(id, product_id)

Remove Product from Collection

Remove a product from a collection.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::CollectionsApi.new
id = 'col_123' # String | Collection ID
product_id = 'prod_123' # String | Product ID

begin
  # Remove Product from Collection
  result = api_instance.collections_delete_product(id, product_id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling CollectionsApi->collections_delete_product: #{e}"
end
```

#### Using the collections_delete_product_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CollectionProductDeletedResponseDto>, Integer, Hash)> collections_delete_product_with_http_info(id, product_id)

```ruby
begin
  # Remove Product from Collection
  data, status_code, headers = api_instance.collections_delete_product_with_http_info(id, product_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CollectionProductDeletedResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling CollectionsApi->collections_delete_product_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Collection ID |  |
| **product_id** | **String** | Product ID |  |

### Return type

[**CollectionProductDeletedResponseDto**](CollectionProductDeletedResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## collections_get

> <CollectionDetailResponseDto> collections_get(id)

Retrieve Collection

Get properties of a product collection by ID.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::CollectionsApi.new
id = 'col_123' # String | Collection ID

begin
  # Retrieve Collection
  result = api_instance.collections_get(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling CollectionsApi->collections_get: #{e}"
end
```

#### Using the collections_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CollectionDetailResponseDto>, Integer, Hash)> collections_get_with_http_info(id)

```ruby
begin
  # Retrieve Collection
  data, status_code, headers = api_instance.collections_get_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CollectionDetailResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling CollectionsApi->collections_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Collection ID |  |

### Return type

[**CollectionDetailResponseDto**](CollectionDetailResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## collections_list

> <Array<CollectionResponseDto>> collections_list

List Collections

Get all active product collections linked to the current active business.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::CollectionsApi.new

begin
  # List Collections
  result = api_instance.collections_list
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling CollectionsApi->collections_list: #{e}"
end
```

#### Using the collections_list_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<CollectionResponseDto>>, Integer, Hash)> collections_list_with_http_info

```ruby
begin
  # List Collections
  data, status_code, headers = api_instance.collections_list_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<CollectionResponseDto>>
rescue Solifyn::ApiError => e
  puts "Error when calling CollectionsApi->collections_list_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;CollectionResponseDto&gt;**](CollectionResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## collections_list_archived

> <Array<CollectionResponseDto>> collections_list_archived

List Archived Collections

Get all archived/deactivated product collections.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::CollectionsApi.new

begin
  # List Archived Collections
  result = api_instance.collections_list_archived
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling CollectionsApi->collections_list_archived: #{e}"
end
```

#### Using the collections_list_archived_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<CollectionResponseDto>>, Integer, Hash)> collections_list_archived_with_http_info

```ruby
begin
  # List Archived Collections
  data, status_code, headers = api_instance.collections_list_archived_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<CollectionResponseDto>>
rescue Solifyn::ApiError => e
  puts "Error when calling CollectionsApi->collections_list_archived_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;CollectionResponseDto&gt;**](CollectionResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## collections_unarchive

> <CollectionUnarchivedResponseDto> collections_unarchive(id)

Unarchive Collection

Restore an archived collection back to active status.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::CollectionsApi.new
id = 'col_123' # String | Collection ID

begin
  # Unarchive Collection
  result = api_instance.collections_unarchive(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling CollectionsApi->collections_unarchive: #{e}"
end
```

#### Using the collections_unarchive_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CollectionUnarchivedResponseDto>, Integer, Hash)> collections_unarchive_with_http_info(id)

```ruby
begin
  # Unarchive Collection
  data, status_code, headers = api_instance.collections_unarchive_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CollectionUnarchivedResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling CollectionsApi->collections_unarchive_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Collection ID |  |

### Return type

[**CollectionUnarchivedResponseDto**](CollectionUnarchivedResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## collections_update

> <CollectionUpdatedResponseDto> collections_update(id, update_collection_dto)

Update Collection

Update products, friendly name, status, or description of a collection.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::CollectionsApi.new
id = 'col_123' # String | Collection ID
update_collection_dto = Solifyn::UpdateCollectionDto.new # UpdateCollectionDto | 

begin
  # Update Collection
  result = api_instance.collections_update(id, update_collection_dto)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling CollectionsApi->collections_update: #{e}"
end
```

#### Using the collections_update_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CollectionUpdatedResponseDto>, Integer, Hash)> collections_update_with_http_info(id, update_collection_dto)

```ruby
begin
  # Update Collection
  data, status_code, headers = api_instance.collections_update_with_http_info(id, update_collection_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CollectionUpdatedResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling CollectionsApi->collections_update_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Collection ID |  |
| **update_collection_dto** | [**UpdateCollectionDto**](UpdateCollectionDto.md) |  |  |

### Return type

[**CollectionUpdatedResponseDto**](CollectionUpdatedResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## collections_update_product

> <CollectionProductUpdatedResponseDto> collections_update_product(id, product_id, update_collection_product_dto)

Update Collection Product

Update quantity of a specific product inside a collection.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::CollectionsApi.new
id = 'col_123' # String | Collection ID
product_id = 'prod_123' # String | Product ID
update_collection_product_dto = Solifyn::UpdateCollectionProductDto.new({quantity: 2}) # UpdateCollectionProductDto | 

begin
  # Update Collection Product
  result = api_instance.collections_update_product(id, product_id, update_collection_product_dto)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling CollectionsApi->collections_update_product: #{e}"
end
```

#### Using the collections_update_product_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CollectionProductUpdatedResponseDto>, Integer, Hash)> collections_update_product_with_http_info(id, product_id, update_collection_product_dto)

```ruby
begin
  # Update Collection Product
  data, status_code, headers = api_instance.collections_update_product_with_http_info(id, product_id, update_collection_product_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CollectionProductUpdatedResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling CollectionsApi->collections_update_product_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Collection ID |  |
| **product_id** | **String** | Product ID |  |
| **update_collection_product_dto** | [**UpdateCollectionProductDto**](UpdateCollectionProductDto.md) |  |  |

### Return type

[**CollectionProductUpdatedResponseDto**](CollectionProductUpdatedResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

