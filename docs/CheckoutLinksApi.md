# Solifyn::CheckoutLinksApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**checkout_links_create**](CheckoutLinksApi.md#checkout_links_create) | **POST** /v1/checkout-links | Create Checkout Link |
| [**checkout_links_delete**](CheckoutLinksApi.md#checkout_links_delete) | **DELETE** /v1/checkout-links/{id} | Delete Checkout Link |
| [**checkout_links_get**](CheckoutLinksApi.md#checkout_links_get) | **GET** /v1/checkout-links/{id} | Retrieve Checkout Link Details |
| [**checkout_links_list**](CheckoutLinksApi.md#checkout_links_list) | **GET** /v1/checkout-links | List Checkout Links |
| [**checkout_links_update**](CheckoutLinksApi.md#checkout_links_update) | **PATCH** /v1/checkout-links/{id} | Update Checkout Link |


## checkout_links_create

> <CheckoutLinkResponseDto> checkout_links_create(create_checkout_link_dto)

Create Checkout Link

Generate a new checkout session link.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::CheckoutLinksApi.new
create_checkout_link_dto = Solifyn::CreateCheckoutLinkDto.new({product_id: 'prod_123'}) # CreateCheckoutLinkDto | 

begin
  # Create Checkout Link
  result = api_instance.checkout_links_create(create_checkout_link_dto)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling CheckoutLinksApi->checkout_links_create: #{e}"
end
```

#### Using the checkout_links_create_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CheckoutLinkResponseDto>, Integer, Hash)> checkout_links_create_with_http_info(create_checkout_link_dto)

```ruby
begin
  # Create Checkout Link
  data, status_code, headers = api_instance.checkout_links_create_with_http_info(create_checkout_link_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CheckoutLinkResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling CheckoutLinksApi->checkout_links_create_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_checkout_link_dto** | [**CreateCheckoutLinkDto**](CreateCheckoutLinkDto.md) |  |  |

### Return type

[**CheckoutLinkResponseDto**](CheckoutLinkResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## checkout_links_delete

> <CheckoutLinkMessageResponseDto> checkout_links_delete(id)

Delete Checkout Link

Permanently remove a checkout link.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::CheckoutLinksApi.new
id = 'chk_123' # String | Checkout Link ID

begin
  # Delete Checkout Link
  result = api_instance.checkout_links_delete(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling CheckoutLinksApi->checkout_links_delete: #{e}"
end
```

#### Using the checkout_links_delete_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CheckoutLinkMessageResponseDto>, Integer, Hash)> checkout_links_delete_with_http_info(id)

```ruby
begin
  # Delete Checkout Link
  data, status_code, headers = api_instance.checkout_links_delete_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CheckoutLinkMessageResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling CheckoutLinksApi->checkout_links_delete_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Checkout Link ID |  |

### Return type

[**CheckoutLinkMessageResponseDto**](CheckoutLinkMessageResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## checkout_links_get

> <CheckoutLinkResponseDto> checkout_links_get(id)

Retrieve Checkout Link Details

Get details of a specific checkout link by ID (public access).

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::CheckoutLinksApi.new
id = 'chk_123' # String | Checkout Link ID

begin
  # Retrieve Checkout Link Details
  result = api_instance.checkout_links_get(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling CheckoutLinksApi->checkout_links_get: #{e}"
end
```

#### Using the checkout_links_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CheckoutLinkResponseDto>, Integer, Hash)> checkout_links_get_with_http_info(id)

```ruby
begin
  # Retrieve Checkout Link Details
  data, status_code, headers = api_instance.checkout_links_get_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CheckoutLinkResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling CheckoutLinksApi->checkout_links_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Checkout Link ID |  |

### Return type

[**CheckoutLinkResponseDto**](CheckoutLinkResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## checkout_links_list

> <Array<CheckoutLinkResponseDto>> checkout_links_list

List Checkout Links

Retrieve all active checkout session links for the active business.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::CheckoutLinksApi.new

begin
  # List Checkout Links
  result = api_instance.checkout_links_list
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling CheckoutLinksApi->checkout_links_list: #{e}"
end
```

#### Using the checkout_links_list_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<CheckoutLinkResponseDto>>, Integer, Hash)> checkout_links_list_with_http_info

```ruby
begin
  # List Checkout Links
  data, status_code, headers = api_instance.checkout_links_list_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<CheckoutLinkResponseDto>>
rescue Solifyn::ApiError => e
  puts "Error when calling CheckoutLinksApi->checkout_links_list_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;CheckoutLinkResponseDto&gt;**](CheckoutLinkResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## checkout_links_update

> <CheckoutLinkMessageResponseDto> checkout_links_update(id, update_checkout_link_dto)

Update Checkout Link

Update title, custom pricing, redirection URLs, or friendly inputs for a checkout link.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::CheckoutLinksApi.new
id = 'chk_123' # String | Checkout Link ID
update_checkout_link_dto = Solifyn::UpdateCheckoutLinkDto.new # UpdateCheckoutLinkDto | 

begin
  # Update Checkout Link
  result = api_instance.checkout_links_update(id, update_checkout_link_dto)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling CheckoutLinksApi->checkout_links_update: #{e}"
end
```

#### Using the checkout_links_update_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CheckoutLinkMessageResponseDto>, Integer, Hash)> checkout_links_update_with_http_info(id, update_checkout_link_dto)

```ruby
begin
  # Update Checkout Link
  data, status_code, headers = api_instance.checkout_links_update_with_http_info(id, update_checkout_link_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CheckoutLinkMessageResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling CheckoutLinksApi->checkout_links_update_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Checkout Link ID |  |
| **update_checkout_link_dto** | [**UpdateCheckoutLinkDto**](UpdateCheckoutLinkDto.md) |  |  |

### Return type

[**CheckoutLinkMessageResponseDto**](CheckoutLinkMessageResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

