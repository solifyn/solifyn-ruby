# Solifyn::ProductAddOnsApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**products_create_addon**](ProductAddOnsApi.md#products_create_addon) | **POST** /v1/products/{id}/addons | Create Product Add-on |
| [**products_delete_addon**](ProductAddOnsApi.md#products_delete_addon) | **DELETE** /v1/products/{id}/addons/{addonId} | Delete Product Add-on |
| [**products_get_addon**](ProductAddOnsApi.md#products_get_addon) | **GET** /v1/products/{id}/addons/{addonId} | Retrieve Product Add-on |
| [**products_list_addons**](ProductAddOnsApi.md#products_list_addons) | **GET** /v1/products/{id}/addons | List Product Add-ons |
| [**products_list_all_addons**](ProductAddOnsApi.md#products_list_all_addons) | **GET** /v1/products/all-addons/list | List All Add-ons |
| [**products_update_addon**](ProductAddOnsApi.md#products_update_addon) | **PATCH** /v1/products/{id}/addons/{addonId} | Update Product Add-on |


## products_create_addon

> <Addon> products_create_addon(id, addon_create)

Create Product Add-on

Attach a new add-on configuration to a product.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::ProductAddOnsApi.new
id = 'prod_parent_123' # String | The parent product ID.
addon_create = Solifyn::AddonCreate.new({product_id: 'prod_addon_123', min_quantity: 0, is_seat_addon: true}) # AddonCreate | 

begin
  # Create Product Add-on
  result = api_instance.products_create_addon(id, addon_create)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling ProductAddOnsApi->products_create_addon: #{e}"
end
```

#### Using the products_create_addon_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Addon>, Integer, Hash)> products_create_addon_with_http_info(id, addon_create)

```ruby
begin
  # Create Product Add-on
  data, status_code, headers = api_instance.products_create_addon_with_http_info(id, addon_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Addon>
rescue Solifyn::ApiError => e
  puts "Error when calling ProductAddOnsApi->products_create_addon_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The parent product ID. |  |
| **addon_create** | [**AddonCreate**](AddonCreate.md) |  |  |

### Return type

[**Addon**](Addon.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## products_delete_addon

> <ProductMessageResponseDto> products_delete_addon(id, addon_id)

Delete Product Add-on

Remove an add-on configuration from a product.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::ProductAddOnsApi.new
id = 'prod_parent_123' # String | The parent product ID.
addon_id = 'prod_addon_123' # String | The add-on product ID to remove.

begin
  # Delete Product Add-on
  result = api_instance.products_delete_addon(id, addon_id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling ProductAddOnsApi->products_delete_addon: #{e}"
end
```

#### Using the products_delete_addon_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ProductMessageResponseDto>, Integer, Hash)> products_delete_addon_with_http_info(id, addon_id)

```ruby
begin
  # Delete Product Add-on
  data, status_code, headers = api_instance.products_delete_addon_with_http_info(id, addon_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ProductMessageResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling ProductAddOnsApi->products_delete_addon_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The parent product ID. |  |
| **addon_id** | **String** | The add-on product ID to remove. |  |

### Return type

[**ProductMessageResponseDto**](ProductMessageResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## products_get_addon

> <Addon> products_get_addon(id, addon_id)

Retrieve Product Add-on

Retrieve a specific add-on configuration of a product.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::ProductAddOnsApi.new
id = 'prod_parent_123' # String | The parent product ID.
addon_id = 'prod_addon_123' # String | The add-on product ID.

begin
  # Retrieve Product Add-on
  result = api_instance.products_get_addon(id, addon_id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling ProductAddOnsApi->products_get_addon: #{e}"
end
```

#### Using the products_get_addon_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Addon>, Integer, Hash)> products_get_addon_with_http_info(id, addon_id)

```ruby
begin
  # Retrieve Product Add-on
  data, status_code, headers = api_instance.products_get_addon_with_http_info(id, addon_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Addon>
rescue Solifyn::ApiError => e
  puts "Error when calling ProductAddOnsApi->products_get_addon_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The parent product ID. |  |
| **addon_id** | **String** | The add-on product ID. |  |

### Return type

[**Addon**](Addon.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## products_list_addons

> <Array<Addon>> products_list_addons(id)

List Product Add-ons

Retrieve all add-on configurations attached to a product.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::ProductAddOnsApi.new
id = 'prod_parent_123' # String | The parent product ID.

begin
  # List Product Add-ons
  result = api_instance.products_list_addons(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling ProductAddOnsApi->products_list_addons: #{e}"
end
```

#### Using the products_list_addons_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Addon>>, Integer, Hash)> products_list_addons_with_http_info(id)

```ruby
begin
  # List Product Add-ons
  data, status_code, headers = api_instance.products_list_addons_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Addon>>
rescue Solifyn::ApiError => e
  puts "Error when calling ProductAddOnsApi->products_list_addons_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The parent product ID. |  |

### Return type

[**Array&lt;Addon&gt;**](Addon.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## products_list_all_addons

> products_list_all_addons

List All Add-ons

Retrieve all configured add-on configurations for the active business.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::ProductAddOnsApi.new

begin
  # List All Add-ons
  api_instance.products_list_all_addons
rescue Solifyn::ApiError => e
  puts "Error when calling ProductAddOnsApi->products_list_all_addons: #{e}"
end
```

#### Using the products_list_all_addons_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> products_list_all_addons_with_http_info

```ruby
begin
  # List All Add-ons
  data, status_code, headers = api_instance.products_list_all_addons_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling ProductAddOnsApi->products_list_all_addons_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## products_update_addon

> <Addon> products_update_addon(id, addon_id, addon_update)

Update Product Add-on

Update an existing add-on configuration for a product.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::ProductAddOnsApi.new
id = 'prod_parent_123' # String | The parent product ID.
addon_id = 'prod_addon_123' # String | The add-on product ID.
addon_update = Solifyn::AddonUpdate.new # AddonUpdate | 

begin
  # Update Product Add-on
  result = api_instance.products_update_addon(id, addon_id, addon_update)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling ProductAddOnsApi->products_update_addon: #{e}"
end
```

#### Using the products_update_addon_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Addon>, Integer, Hash)> products_update_addon_with_http_info(id, addon_id, addon_update)

```ruby
begin
  # Update Product Add-on
  data, status_code, headers = api_instance.products_update_addon_with_http_info(id, addon_id, addon_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Addon>
rescue Solifyn::ApiError => e
  puts "Error when calling ProductAddOnsApi->products_update_addon_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The parent product ID. |  |
| **addon_id** | **String** | The add-on product ID. |  |
| **addon_update** | [**AddonUpdate**](AddonUpdate.md) |  |  |

### Return type

[**Addon**](Addon.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

