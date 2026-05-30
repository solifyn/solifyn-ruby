# Solifyn::BrandsApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**brands_create**](BrandsApi.md#brands_create) | **POST** /v1/user/brand | Create Brand |
| [**brands_get**](BrandsApi.md#brands_get) | **GET** /v1/user/brand/{id} | Retrieve Brand |
| [**brands_list**](BrandsApi.md#brands_list) | **GET** /v1/user/brands | List Brands |
| [**brands_update**](BrandsApi.md#brands_update) | **PATCH** /v1/user/brand/{id} | Update Brand |


## brands_create

> <Brand> brands_create(brand_create)

Create Brand

Add a new brand identity under the current active business.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::BrandsApi.new
brand_create = Solifyn::BrandCreate.new({name: 'Acme Corp'}) # BrandCreate | 

begin
  # Create Brand
  result = api_instance.brands_create(brand_create)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling BrandsApi->brands_create: #{e}"
end
```

#### Using the brands_create_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Brand>, Integer, Hash)> brands_create_with_http_info(brand_create)

```ruby
begin
  # Create Brand
  data, status_code, headers = api_instance.brands_create_with_http_info(brand_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Brand>
rescue Solifyn::ApiError => e
  puts "Error when calling BrandsApi->brands_create_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **brand_create** | [**BrandCreate**](BrandCreate.md) |  |  |

### Return type

[**Brand**](Brand.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## brands_get

> <Brand> brands_get(id)

Retrieve Brand

Retrieve details of a brand identity by ID.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::BrandsApi.new
id = 'brd_123' # String | The brand ID to retrieve

begin
  # Retrieve Brand
  result = api_instance.brands_get(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling BrandsApi->brands_get: #{e}"
end
```

#### Using the brands_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Brand>, Integer, Hash)> brands_get_with_http_info(id)

```ruby
begin
  # Retrieve Brand
  data, status_code, headers = api_instance.brands_get_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Brand>
rescue Solifyn::ApiError => e
  puts "Error when calling BrandsApi->brands_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The brand ID to retrieve |  |

### Return type

[**Brand**](Brand.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## brands_list

> <Array<Brand>> brands_list

List Brands

Retrieve all brands associated with the current business context.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::BrandsApi.new

begin
  # List Brands
  result = api_instance.brands_list
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling BrandsApi->brands_list: #{e}"
end
```

#### Using the brands_list_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Brand>>, Integer, Hash)> brands_list_with_http_info

```ruby
begin
  # List Brands
  data, status_code, headers = api_instance.brands_list_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Brand>>
rescue Solifyn::ApiError => e
  puts "Error when calling BrandsApi->brands_list_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;Brand&gt;**](Brand.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## brands_update

> <Brand> brands_update(id, brand_update)

Update Brand

Update website, logo, description, or statement descriptors of a brand.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::BrandsApi.new
id = 'brd_123' # String | The brand ID to update
brand_update = Solifyn::BrandUpdate.new # BrandUpdate | 

begin
  # Update Brand
  result = api_instance.brands_update(id, brand_update)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling BrandsApi->brands_update: #{e}"
end
```

#### Using the brands_update_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Brand>, Integer, Hash)> brands_update_with_http_info(id, brand_update)

```ruby
begin
  # Update Brand
  data, status_code, headers = api_instance.brands_update_with_http_info(id, brand_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Brand>
rescue Solifyn::ApiError => e
  puts "Error when calling BrandsApi->brands_update_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The brand ID to update |  |
| **brand_update** | [**BrandUpdate**](BrandUpdate.md) |  |  |

### Return type

[**Brand**](Brand.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

