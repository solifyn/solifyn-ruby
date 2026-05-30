# Solifyn::CustomersApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**customers_create**](CustomersApi.md#customers_create) | **POST** /v1/customers | Create Customer |
| [**customers_generate_invite**](CustomersApi.md#customers_generate_invite) | **POST** /v1/customers/{id}/share | Generate Shared Invite |
| [**customers_get**](CustomersApi.md#customers_get) | **GET** /v1/customers/{id} | Retrieve Customer |
| [**customers_list**](CustomersApi.md#customers_list) | **GET** /v1/customers | List Customers |
| [**customers_update**](CustomersApi.md#customers_update) | **PATCH** /v1/customers/{id} | Update Customer |


## customers_create

> <CustomerResponseDto> customers_create(create_customer_dto)

Create Customer

Add/upsert a new customer profile under the current business context.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::CustomersApi.new
create_customer_dto = Solifyn::CreateCustomerDto.new({email: 'customer@gmail.com', name: 'John Doe'}) # CreateCustomerDto | 

begin
  # Create Customer
  result = api_instance.customers_create(create_customer_dto)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling CustomersApi->customers_create: #{e}"
end
```

#### Using the customers_create_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerResponseDto>, Integer, Hash)> customers_create_with_http_info(create_customer_dto)

```ruby
begin
  # Create Customer
  data, status_code, headers = api_instance.customers_create_with_http_info(create_customer_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling CustomersApi->customers_create_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_customer_dto** | [**CreateCustomerDto**](CreateCustomerDto.md) |  |  |

### Return type

[**CustomerResponseDto**](CustomerResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## customers_generate_invite

> <CustomerSharedInviteResponseDto> customers_generate_invite(id)

Generate Shared Invite

Generate a short-lived token granting temporary customer self-service billing page access.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::CustomersApi.new
id = 'user_123' # String | Customer ID

begin
  # Generate Shared Invite
  result = api_instance.customers_generate_invite(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling CustomersApi->customers_generate_invite: #{e}"
end
```

#### Using the customers_generate_invite_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerSharedInviteResponseDto>, Integer, Hash)> customers_generate_invite_with_http_info(id)

```ruby
begin
  # Generate Shared Invite
  data, status_code, headers = api_instance.customers_generate_invite_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerSharedInviteResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling CustomersApi->customers_generate_invite_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Customer ID |  |

### Return type

[**CustomerSharedInviteResponseDto**](CustomerSharedInviteResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## customers_get

> <CustomerResponseDto> customers_get(id)

Retrieve Customer

Retrieve details of a customer profile by ID.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::CustomersApi.new
id = 'user_123' # String | Customer ID

begin
  # Retrieve Customer
  result = api_instance.customers_get(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling CustomersApi->customers_get: #{e}"
end
```

#### Using the customers_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerResponseDto>, Integer, Hash)> customers_get_with_http_info(id)

```ruby
begin
  # Retrieve Customer
  data, status_code, headers = api_instance.customers_get_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling CustomersApi->customers_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Customer ID |  |

### Return type

[**CustomerResponseDto**](CustomerResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## customers_list

> <CustomerListResponseDto> customers_list

List Customers

Retrieve all customers associated with the current active business.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::CustomersApi.new

begin
  # List Customers
  result = api_instance.customers_list
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling CustomersApi->customers_list: #{e}"
end
```

#### Using the customers_list_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerListResponseDto>, Integer, Hash)> customers_list_with_http_info

```ruby
begin
  # List Customers
  data, status_code, headers = api_instance.customers_list_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerListResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling CustomersApi->customers_list_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**CustomerListResponseDto**](CustomerListResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## customers_update

> <CustomerMessageResponseDto> customers_update(id, update_customer_dto)

Update Customer

Update name, phone, or metadata of an existing customer profile.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::CustomersApi.new
id = 'user_123' # String | Customer ID
update_customer_dto = Solifyn::UpdateCustomerDto.new # UpdateCustomerDto | 

begin
  # Update Customer
  result = api_instance.customers_update(id, update_customer_dto)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling CustomersApi->customers_update: #{e}"
end
```

#### Using the customers_update_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerMessageResponseDto>, Integer, Hash)> customers_update_with_http_info(id, update_customer_dto)

```ruby
begin
  # Update Customer
  data, status_code, headers = api_instance.customers_update_with_http_info(id, update_customer_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerMessageResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling CustomersApi->customers_update_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Customer ID |  |
| **update_customer_dto** | [**UpdateCustomerDto**](UpdateCustomerDto.md) |  |  |

### Return type

[**CustomerMessageResponseDto**](CustomerMessageResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

