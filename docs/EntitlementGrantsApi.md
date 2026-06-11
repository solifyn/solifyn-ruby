# Solifyn::EntitlementGrantsApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**entitlement_grants_get**](EntitlementGrantsApi.md#entitlement_grants_get) | **GET** /v1/entitlement-grants/{id} | Retrieve Entitlement Grant |
| [**entitlement_grants_list**](EntitlementGrantsApi.md#entitlement_grants_list) | **GET** /v1/entitlement-grants | List Entitlement Grants |
| [**entitlement_grants_retry**](EntitlementGrantsApi.md#entitlement_grants_retry) | **POST** /v1/entitlement-grants/{id}/retry | Retry Entitlement Grant Delivery |
| [**entitlement_grants_revoke**](EntitlementGrantsApi.md#entitlement_grants_revoke) | **POST** /v1/entitlement-grants/{id}/revoke | Manually Revoke Entitlement Grant |


## entitlement_grants_get

> <EntitlementGrantResponseDto> entitlement_grants_get(id)

Retrieve Entitlement Grant

Retrieve details of a specific entitlement grant.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::EntitlementGrantsApi.new
id = 'id_example' # String | The unique grant ID

begin
  # Retrieve Entitlement Grant
  result = api_instance.entitlement_grants_get(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling EntitlementGrantsApi->entitlement_grants_get: #{e}"
end
```

#### Using the entitlement_grants_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<EntitlementGrantResponseDto>, Integer, Hash)> entitlement_grants_get_with_http_info(id)

```ruby
begin
  # Retrieve Entitlement Grant
  data, status_code, headers = api_instance.entitlement_grants_get_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <EntitlementGrantResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling EntitlementGrantsApi->entitlement_grants_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique grant ID |  |

### Return type

[**EntitlementGrantResponseDto**](EntitlementGrantResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## entitlement_grants_list

> <Array<EntitlementGrantResponseDto>> entitlement_grants_list(opts)

List Entitlement Grants

Retrieve all GitHub repository entitlement grants for the active business.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::EntitlementGrantsApi.new
opts = {
  status: 'status_example', # String | Filter by status (PENDING, DELIVERED, FAILED, REVOKED)
  entitlement_id: 'entitlement_id_example', # String | Filter by entitlement config ID
  product_id: 'product_id_example' # String | Filter by product ID
}

begin
  # List Entitlement Grants
  result = api_instance.entitlement_grants_list(opts)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling EntitlementGrantsApi->entitlement_grants_list: #{e}"
end
```

#### Using the entitlement_grants_list_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<EntitlementGrantResponseDto>>, Integer, Hash)> entitlement_grants_list_with_http_info(opts)

```ruby
begin
  # List Entitlement Grants
  data, status_code, headers = api_instance.entitlement_grants_list_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<EntitlementGrantResponseDto>>
rescue Solifyn::ApiError => e
  puts "Error when calling EntitlementGrantsApi->entitlement_grants_list_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** | Filter by status (PENDING, DELIVERED, FAILED, REVOKED) | [optional] |
| **entitlement_id** | **String** | Filter by entitlement config ID | [optional] |
| **product_id** | **String** | Filter by product ID | [optional] |

### Return type

[**Array&lt;EntitlementGrantResponseDto&gt;**](EntitlementGrantResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## entitlement_grants_retry

> <EntitlementGrantResponseDto> entitlement_grants_retry(id)

Retry Entitlement Grant Delivery

Attempts to re-invite the collaborator if GitHub username is already connected, or resets the OAuth URL redirect.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::EntitlementGrantsApi.new
id = 'id_example' # String | The unique grant ID

begin
  # Retry Entitlement Grant Delivery
  result = api_instance.entitlement_grants_retry(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling EntitlementGrantsApi->entitlement_grants_retry: #{e}"
end
```

#### Using the entitlement_grants_retry_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<EntitlementGrantResponseDto>, Integer, Hash)> entitlement_grants_retry_with_http_info(id)

```ruby
begin
  # Retry Entitlement Grant Delivery
  data, status_code, headers = api_instance.entitlement_grants_retry_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <EntitlementGrantResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling EntitlementGrantsApi->entitlement_grants_retry_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique grant ID |  |

### Return type

[**EntitlementGrantResponseDto**](EntitlementGrantResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## entitlement_grants_revoke

> <EntitlementGrantResponseDto> entitlement_grants_revoke(id)

Manually Revoke Entitlement Grant

Manually remove the customer collaborator access from the repository and revoke the grant.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::EntitlementGrantsApi.new
id = 'id_example' # String | The unique grant ID

begin
  # Manually Revoke Entitlement Grant
  result = api_instance.entitlement_grants_revoke(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling EntitlementGrantsApi->entitlement_grants_revoke: #{e}"
end
```

#### Using the entitlement_grants_revoke_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<EntitlementGrantResponseDto>, Integer, Hash)> entitlement_grants_revoke_with_http_info(id)

```ruby
begin
  # Manually Revoke Entitlement Grant
  data, status_code, headers = api_instance.entitlement_grants_revoke_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <EntitlementGrantResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling EntitlementGrantsApi->entitlement_grants_revoke_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique grant ID |  |

### Return type

[**EntitlementGrantResponseDto**](EntitlementGrantResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

