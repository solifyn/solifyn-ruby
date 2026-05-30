# Solifyn::ProductsApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**products_archive**](ProductsApi.md#products_archive) | **DELETE** /v1/products/{id} | Archive Product |
| [**products_create**](ProductsApi.md#products_create) | **POST** /v1/products | Create Product |
| [**products_get**](ProductsApi.md#products_get) | **GET** /v1/products/{id} | Retrieve Product |
| [**products_list**](ProductsApi.md#products_list) | **GET** /v1/products | List Products |
| [**products_unarchive**](ProductsApi.md#products_unarchive) | **POST** /v1/products/{id}/unarchive | Unarchive Product |
| [**products_update**](ProductsApi.md#products_update) | **PATCH** /v1/products/{id} | Update Product |


## products_archive

> <ProductsArchive200Response> products_archive(id)

Archive Product

Archive a specific product to hide it from checkout pages and search results. Products are soft-deleted (archived) and can be restored using the unarchive endpoint.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::ProductsApi.new
id = 'prod_123' # String | The unique product ID to archive.

begin
  # Archive Product
  result = api_instance.products_archive(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling ProductsApi->products_archive: #{e}"
end
```

#### Using the products_archive_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ProductsArchive200Response>, Integer, Hash)> products_archive_with_http_info(id)

```ruby
begin
  # Archive Product
  data, status_code, headers = api_instance.products_archive_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ProductsArchive200Response>
rescue Solifyn::ApiError => e
  puts "Error when calling ProductsApi->products_archive_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique product ID to archive. |  |

### Return type

[**ProductsArchive200Response**](ProductsArchive200Response.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## products_create

> <Product> products_create(product_create)

Create Product

Create a new product within your active business.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::ProductsApi.new
product_create = Solifyn::ProductCreate.new({name: 'Enterprise SaaS Plan', price: 99, currency: 'USD', tax_category: 'digital_products'}) # ProductCreate | 

begin
  # Create Product
  result = api_instance.products_create(product_create)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling ProductsApi->products_create: #{e}"
end
```

#### Using the products_create_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Product>, Integer, Hash)> products_create_with_http_info(product_create)

```ruby
begin
  # Create Product
  data, status_code, headers = api_instance.products_create_with_http_info(product_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Product>
rescue Solifyn::ApiError => e
  puts "Error when calling ProductsApi->products_create_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_create** | [**ProductCreate**](ProductCreate.md) |  |  |

### Return type

[**Product**](Product.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## products_get

> <Product> products_get(id)

Retrieve Product

Retrieve details of a specific product using its ID.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::ProductsApi.new
id = 'prod_123' # String | The unique product ID.

begin
  # Retrieve Product
  result = api_instance.products_get(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling ProductsApi->products_get: #{e}"
end
```

#### Using the products_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Product>, Integer, Hash)> products_get_with_http_info(id)

```ruby
begin
  # Retrieve Product
  data, status_code, headers = api_instance.products_get_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Product>
rescue Solifyn::ApiError => e
  puts "Error when calling ProductsApi->products_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique product ID. |  |

### Return type

[**Product**](Product.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## products_list

> <ProductsList200Response> products_list(opts)

List Products

List and query products belonging to your active business with support for fuzzy search, filters, pagination, and sorting.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::ProductsApi.new
opts = {
  pricing_type: 'pricing_type_example', # String | Filter by pricing type.
  sorting: 'created_at', # String | Sorting criterion. Add a minus sign - before the criteria name to sort by descending order.
  limit: 8.14, # Float | Size of a page, defaults to 10. Maximum is 100.
  page: 8.14, # Float | Page number, defaults to 1.
  is_recurring: true, # Boolean | Filter on recurring products (subscriptions). If true, only subscription tiers are returned. If false, only one-time purchase products are returned.
  is_archived: true, # Boolean | Filter by archived status.
  query: 'query_example', # String | Filter by product name (fuzzy, case-insensitive).
  id: 'id_example' # String | Filter by product ID.
}

begin
  # List Products
  result = api_instance.products_list(opts)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling ProductsApi->products_list: #{e}"
end
```

#### Using the products_list_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ProductsList200Response>, Integer, Hash)> products_list_with_http_info(opts)

```ruby
begin
  # List Products
  data, status_code, headers = api_instance.products_list_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ProductsList200Response>
rescue Solifyn::ApiError => e
  puts "Error when calling ProductsApi->products_list_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **pricing_type** | **String** | Filter by pricing type. | [optional] |
| **sorting** | **String** | Sorting criterion. Add a minus sign - before the criteria name to sort by descending order. | [optional] |
| **limit** | **Float** | Size of a page, defaults to 10. Maximum is 100. | [optional][default to 10] |
| **page** | **Float** | Page number, defaults to 1. | [optional][default to 1] |
| **is_recurring** | **Boolean** | Filter on recurring products (subscriptions). If true, only subscription tiers are returned. If false, only one-time purchase products are returned. | [optional] |
| **is_archived** | **Boolean** | Filter by archived status. | [optional] |
| **query** | **String** | Filter by product name (fuzzy, case-insensitive). | [optional] |
| **id** | **String** | Filter by product ID. | [optional] |

### Return type

[**ProductsList200Response**](ProductsList200Response.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## products_unarchive

> <ProductsUnarchive200Response> products_unarchive(id)

Unarchive Product

Restore an archived product back to active status, making it visible again.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::ProductsApi.new
id = 'prod_123' # String | The unique product ID to unarchive.

begin
  # Unarchive Product
  result = api_instance.products_unarchive(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling ProductsApi->products_unarchive: #{e}"
end
```

#### Using the products_unarchive_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ProductsUnarchive200Response>, Integer, Hash)> products_unarchive_with_http_info(id)

```ruby
begin
  # Unarchive Product
  data, status_code, headers = api_instance.products_unarchive_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ProductsUnarchive200Response>
rescue Solifyn::ApiError => e
  puts "Error when calling ProductsApi->products_unarchive_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique product ID to unarchive. |  |

### Return type

[**ProductsUnarchive200Response**](ProductsUnarchive200Response.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## products_update

> <ProductMessageResponseDto> products_update(id, product_update)

Update Product

Update details of an existing product.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::ProductsApi.new
id = 'prod_123' # String | The unique product ID.
product_update = Solifyn::ProductUpdate.new # ProductUpdate | 

begin
  # Update Product
  result = api_instance.products_update(id, product_update)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling ProductsApi->products_update: #{e}"
end
```

#### Using the products_update_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ProductMessageResponseDto>, Integer, Hash)> products_update_with_http_info(id, product_update)

```ruby
begin
  # Update Product
  data, status_code, headers = api_instance.products_update_with_http_info(id, product_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ProductMessageResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling ProductsApi->products_update_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique product ID. |  |
| **product_update** | [**ProductUpdate**](ProductUpdate.md) |  |  |

### Return type

[**ProductMessageResponseDto**](ProductMessageResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

