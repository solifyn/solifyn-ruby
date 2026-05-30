# Solifyn::DiscountsApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**discounts_create**](DiscountsApi.md#discounts_create) | **POST** /v1/discounts | Create Discount |
| [**discounts_delete**](DiscountsApi.md#discounts_delete) | **DELETE** /v1/discounts/{id} | Delete Discount |
| [**discounts_get**](DiscountsApi.md#discounts_get) | **GET** /v1/discounts/{id} | Retrieve Discount |
| [**discounts_list**](DiscountsApi.md#discounts_list) | **GET** /v1/discounts | List Discounts |
| [**discounts_update**](DiscountsApi.md#discounts_update) | **PATCH** /v1/discounts/{id} | Update Discount |
| [**discounts_validate**](DiscountsApi.md#discounts_validate) | **GET** /v1/discounts/validate | Validate Code |


## discounts_create

> <Discount> discounts_create(discount_create)

Create Discount

Create a new discount code within your active business.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::DiscountsApi.new
discount_create = Solifyn::DiscountCreate.new({code: 'code_example', type: 'percentage', amount: 3.56}) # DiscountCreate | 

begin
  # Create Discount
  result = api_instance.discounts_create(discount_create)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling DiscountsApi->discounts_create: #{e}"
end
```

#### Using the discounts_create_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Discount>, Integer, Hash)> discounts_create_with_http_info(discount_create)

```ruby
begin
  # Create Discount
  data, status_code, headers = api_instance.discounts_create_with_http_info(discount_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Discount>
rescue Solifyn::ApiError => e
  puts "Error when calling DiscountsApi->discounts_create_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **discount_create** | [**DiscountCreate**](DiscountCreate.md) |  |  |

### Return type

[**Discount**](Discount.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## discounts_delete

> <LicensesDeactivate200Response> discounts_delete(id)

Delete Discount

Delete a specific discount code by ID.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::DiscountsApi.new
id = 'disc_123' # String | The unique discount ID.

begin
  # Delete Discount
  result = api_instance.discounts_delete(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling DiscountsApi->discounts_delete: #{e}"
end
```

#### Using the discounts_delete_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<LicensesDeactivate200Response>, Integer, Hash)> discounts_delete_with_http_info(id)

```ruby
begin
  # Delete Discount
  data, status_code, headers = api_instance.discounts_delete_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <LicensesDeactivate200Response>
rescue Solifyn::ApiError => e
  puts "Error when calling DiscountsApi->discounts_delete_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique discount ID. |  |

### Return type

[**LicensesDeactivate200Response**](LicensesDeactivate200Response.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## discounts_get

> <Discount> discounts_get(id)

Retrieve Discount

Retrieve details of a specific discount code using its ID.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::DiscountsApi.new
id = 'disc_123' # String | The unique discount ID.

begin
  # Retrieve Discount
  result = api_instance.discounts_get(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling DiscountsApi->discounts_get: #{e}"
end
```

#### Using the discounts_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Discount>, Integer, Hash)> discounts_get_with_http_info(id)

```ruby
begin
  # Retrieve Discount
  data, status_code, headers = api_instance.discounts_get_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Discount>
rescue Solifyn::ApiError => e
  puts "Error when calling DiscountsApi->discounts_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique discount ID. |  |

### Return type

[**Discount**](Discount.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## discounts_list

> <DiscountsList200Response> discounts_list(opts)

List Discounts

List and query discounts belonging to your active business with support for fuzzy search by code, pagination, and sorting.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::DiscountsApi.new
opts = {
  sorting: 'created_at', # String | Sorting criterion. Add a minus sign - before the criteria name to sort by descending order.
  limit: 8.14, # Float | Size of a page, defaults to 10. Maximum is 100.
  page: 8.14, # Float | Page number, defaults to 1.
  query: 'query_example', # String | Filter by discount code (fuzzy, case-insensitive).
  id: 'id_example' # String | Filter by discount ID.
}

begin
  # List Discounts
  result = api_instance.discounts_list(opts)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling DiscountsApi->discounts_list: #{e}"
end
```

#### Using the discounts_list_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DiscountsList200Response>, Integer, Hash)> discounts_list_with_http_info(opts)

```ruby
begin
  # List Discounts
  data, status_code, headers = api_instance.discounts_list_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DiscountsList200Response>
rescue Solifyn::ApiError => e
  puts "Error when calling DiscountsApi->discounts_list_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sorting** | **String** | Sorting criterion. Add a minus sign - before the criteria name to sort by descending order. | [optional] |
| **limit** | **Float** | Size of a page, defaults to 10. Maximum is 100. | [optional][default to 10] |
| **page** | **Float** | Page number, defaults to 1. | [optional][default to 1] |
| **query** | **String** | Filter by discount code (fuzzy, case-insensitive). | [optional] |
| **id** | **String** | Filter by discount ID. | [optional] |

### Return type

[**DiscountsList200Response**](DiscountsList200Response.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## discounts_update

> <Discount> discounts_update(id, discount_update)

Update Discount

Update details of an existing discount code.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::DiscountsApi.new
id = 'disc_123' # String | The unique discount ID.
discount_update = Solifyn::DiscountUpdate.new # DiscountUpdate | 

begin
  # Update Discount
  result = api_instance.discounts_update(id, discount_update)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling DiscountsApi->discounts_update: #{e}"
end
```

#### Using the discounts_update_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Discount>, Integer, Hash)> discounts_update_with_http_info(id, discount_update)

```ruby
begin
  # Update Discount
  data, status_code, headers = api_instance.discounts_update_with_http_info(id, discount_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Discount>
rescue Solifyn::ApiError => e
  puts "Error when calling DiscountsApi->discounts_update_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique discount ID. |  |
| **discount_update** | [**DiscountUpdate**](DiscountUpdate.md) |  |  |

### Return type

[**Discount**](Discount.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## discounts_validate

> <Discount> discounts_validate(code, business_id)

Validate Code

Validate if a specific discount code is active and valid for purchase checkout.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::DiscountsApi.new
code = 'SAVE20' # String | The plain discount code string
business_id = 'biz_123' # String | The business database ID context

begin
  # Validate Code
  result = api_instance.discounts_validate(code, business_id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling DiscountsApi->discounts_validate: #{e}"
end
```

#### Using the discounts_validate_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Discount>, Integer, Hash)> discounts_validate_with_http_info(code, business_id)

```ruby
begin
  # Validate Code
  data, status_code, headers = api_instance.discounts_validate_with_http_info(code, business_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Discount>
rescue Solifyn::ApiError => e
  puts "Error when calling DiscountsApi->discounts_validate_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **code** | **String** | The plain discount code string |  |
| **business_id** | **String** | The business database ID context |  |

### Return type

[**Discount**](Discount.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

