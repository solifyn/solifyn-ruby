# Solifyn::EntitlementsApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**entitlements_create**](EntitlementsApi.md#entitlements_create) | **POST** /v1/entitlements | Create Entitlement |
| [**entitlements_delete**](EntitlementsApi.md#entitlements_delete) | **DELETE** /v1/entitlements/{id} | Delete Entitlement |
| [**entitlements_get**](EntitlementsApi.md#entitlements_get) | **GET** /v1/entitlements/{id} | Retrieve Entitlement |
| [**entitlements_list**](EntitlementsApi.md#entitlements_list) | **GET** /v1/entitlements | List Entitlements |
| [**entitlements_update**](EntitlementsApi.md#entitlements_update) | **PATCH** /v1/entitlements/{id} | Update Entitlement |


## entitlements_create

> <EntitlementDetailResponseDto> entitlements_create(create_entitlement_dto)

Create Entitlement

Create a new independent access entitlement.

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::EntitlementsApi.new
create_entitlement_dto = Solifyn::CreateEntitlementDto.new({name: 'Premium GitHub Access', type: 'GITHUB'}) # CreateEntitlementDto | 

begin
  # Create Entitlement
  result = api_instance.entitlements_create(create_entitlement_dto)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling EntitlementsApi->entitlements_create: #{e}"
end
```

#### Using the entitlements_create_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<EntitlementDetailResponseDto>, Integer, Hash)> entitlements_create_with_http_info(create_entitlement_dto)

```ruby
begin
  # Create Entitlement
  data, status_code, headers = api_instance.entitlements_create_with_http_info(create_entitlement_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <EntitlementDetailResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling EntitlementsApi->entitlements_create_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_entitlement_dto** | [**CreateEntitlementDto**](CreateEntitlementDto.md) |  |  |

### Return type

[**EntitlementDetailResponseDto**](EntitlementDetailResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## entitlements_delete

> <EntitlementDetailResponseDto> entitlements_delete(id)

Delete Entitlement

Delete an independent entitlement and unlink all mapped products.

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::EntitlementsApi.new
id = 'ent_8Z1aB2cD3eF4gH5iJ6kL7m' # String | The unique entitlement ID.

begin
  # Delete Entitlement
  result = api_instance.entitlements_delete(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling EntitlementsApi->entitlements_delete: #{e}"
end
```

#### Using the entitlements_delete_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<EntitlementDetailResponseDto>, Integer, Hash)> entitlements_delete_with_http_info(id)

```ruby
begin
  # Delete Entitlement
  data, status_code, headers = api_instance.entitlements_delete_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <EntitlementDetailResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling EntitlementsApi->entitlements_delete_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique entitlement ID. |  |

### Return type

[**EntitlementDetailResponseDto**](EntitlementDetailResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## entitlements_get

> <EntitlementDetailResponseDto> entitlements_get(id)

Retrieve Entitlement

Retrieve a specific entitlement definition by ID.

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::EntitlementsApi.new
id = 'ent_8Z1aB2cD3eF4gH5iJ6kL7m' # String | The unique entitlement ID.

begin
  # Retrieve Entitlement
  result = api_instance.entitlements_get(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling EntitlementsApi->entitlements_get: #{e}"
end
```

#### Using the entitlements_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<EntitlementDetailResponseDto>, Integer, Hash)> entitlements_get_with_http_info(id)

```ruby
begin
  # Retrieve Entitlement
  data, status_code, headers = api_instance.entitlements_get_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <EntitlementDetailResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling EntitlementsApi->entitlements_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique entitlement ID. |  |

### Return type

[**EntitlementDetailResponseDto**](EntitlementDetailResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## entitlements_list

> <Array<EntitlementDetailResponseDto>> entitlements_list

List Entitlements

List all independent entitlements for the active business.

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::EntitlementsApi.new

begin
  # List Entitlements
  result = api_instance.entitlements_list
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling EntitlementsApi->entitlements_list: #{e}"
end
```

#### Using the entitlements_list_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<EntitlementDetailResponseDto>>, Integer, Hash)> entitlements_list_with_http_info

```ruby
begin
  # List Entitlements
  data, status_code, headers = api_instance.entitlements_list_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<EntitlementDetailResponseDto>>
rescue Solifyn::ApiError => e
  puts "Error when calling EntitlementsApi->entitlements_list_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;EntitlementDetailResponseDto&gt;**](EntitlementDetailResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## entitlements_update

> <EntitlementDetailResponseDto> entitlements_update(id, update_entitlement_dto)

Update Entitlement

Update details of an existing independent entitlement.

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::EntitlementsApi.new
id = 'ent_8Z1aB2cD3eF4gH5iJ6kL7m' # String | The unique entitlement ID.
update_entitlement_dto = Solifyn::UpdateEntitlementDto.new # UpdateEntitlementDto | 

begin
  # Update Entitlement
  result = api_instance.entitlements_update(id, update_entitlement_dto)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling EntitlementsApi->entitlements_update: #{e}"
end
```

#### Using the entitlements_update_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<EntitlementDetailResponseDto>, Integer, Hash)> entitlements_update_with_http_info(id, update_entitlement_dto)

```ruby
begin
  # Update Entitlement
  data, status_code, headers = api_instance.entitlements_update_with_http_info(id, update_entitlement_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <EntitlementDetailResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling EntitlementsApi->entitlements_update_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique entitlement ID. |  |
| **update_entitlement_dto** | [**UpdateEntitlementDto**](UpdateEntitlementDto.md) |  |  |

### Return type

[**EntitlementDetailResponseDto**](EntitlementDetailResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

