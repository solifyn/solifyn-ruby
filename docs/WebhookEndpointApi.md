# Solifyn::WebhookEndpointApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**operational_webhook_controller_create**](WebhookEndpointApi.md#operational_webhook_controller_create) | **POST** /v1/operational-webhook/endpoint | Create Operational Webhook Endpoint |
| [**operational_webhook_controller_delete**](WebhookEndpointApi.md#operational_webhook_controller_delete) | **DELETE** /v1/operational-webhook/endpoint/{id} | Delete Operational Webhook Endpoint |
| [**operational_webhook_controller_get**](WebhookEndpointApi.md#operational_webhook_controller_get) | **GET** /v1/operational-webhook/endpoint/{id} | Get Operational Webhook Endpoint |
| [**operational_webhook_controller_get_headers**](WebhookEndpointApi.md#operational_webhook_controller_get_headers) | **GET** /v1/operational-webhook/endpoint/{id}/headers | Get Operational Webhook Endpoint Headers |
| [**operational_webhook_controller_get_secret**](WebhookEndpointApi.md#operational_webhook_controller_get_secret) | **GET** /v1/operational-webhook/endpoint/{id}/secret | Get Operational Webhook Endpoint Secret |
| [**operational_webhook_controller_list**](WebhookEndpointApi.md#operational_webhook_controller_list) | **GET** /v1/operational-webhook/endpoint | List Operational Webhook Endpoints |
| [**operational_webhook_controller_rotate_secret**](WebhookEndpointApi.md#operational_webhook_controller_rotate_secret) | **POST** /v1/operational-webhook/endpoint/{id}/secret/rotate | Rotate Operational Webhook Endpoint Secret |
| [**operational_webhook_controller_update**](WebhookEndpointApi.md#operational_webhook_controller_update) | **PUT** /v1/operational-webhook/endpoint/{id} | Update Operational Webhook Endpoint |
| [**operational_webhook_controller_update_headers**](WebhookEndpointApi.md#operational_webhook_controller_update_headers) | **PUT** /v1/operational-webhook/endpoint/{id}/headers | Set Operational Webhook Endpoint Headers |


## operational_webhook_controller_create

> <OperationalWebhookEndpointResponseDto> operational_webhook_controller_create(operational_webhook_endpoint_in_dto)

Create Operational Webhook Endpoint

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::WebhookEndpointApi.new
operational_webhook_endpoint_in_dto = Solifyn::OperationalWebhookEndpointInDto.new({url: 'https://example.com/webhook/'}) # OperationalWebhookEndpointInDto | 

begin
  # Create Operational Webhook Endpoint
  result = api_instance.operational_webhook_controller_create(operational_webhook_endpoint_in_dto)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling WebhookEndpointApi->operational_webhook_controller_create: #{e}"
end
```

#### Using the operational_webhook_controller_create_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<OperationalWebhookEndpointResponseDto>, Integer, Hash)> operational_webhook_controller_create_with_http_info(operational_webhook_endpoint_in_dto)

```ruby
begin
  # Create Operational Webhook Endpoint
  data, status_code, headers = api_instance.operational_webhook_controller_create_with_http_info(operational_webhook_endpoint_in_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <OperationalWebhookEndpointResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling WebhookEndpointApi->operational_webhook_controller_create_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **operational_webhook_endpoint_in_dto** | [**OperationalWebhookEndpointInDto**](OperationalWebhookEndpointInDto.md) |  |  |

### Return type

[**OperationalWebhookEndpointResponseDto**](OperationalWebhookEndpointResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## operational_webhook_controller_delete

> operational_webhook_controller_delete(id)

Delete Operational Webhook Endpoint

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::WebhookEndpointApi.new
id = 'id_example' # String | The endpoint ID or UID

begin
  # Delete Operational Webhook Endpoint
  api_instance.operational_webhook_controller_delete(id)
rescue Solifyn::ApiError => e
  puts "Error when calling WebhookEndpointApi->operational_webhook_controller_delete: #{e}"
end
```

#### Using the operational_webhook_controller_delete_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> operational_webhook_controller_delete_with_http_info(id)

```ruby
begin
  # Delete Operational Webhook Endpoint
  data, status_code, headers = api_instance.operational_webhook_controller_delete_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling WebhookEndpointApi->operational_webhook_controller_delete_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The endpoint ID or UID |  |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## operational_webhook_controller_get

> <OperationalWebhookEndpointResponseDto> operational_webhook_controller_get(id)

Get Operational Webhook Endpoint

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::WebhookEndpointApi.new
id = 'id_example' # String | The endpoint ID or UID

begin
  # Get Operational Webhook Endpoint
  result = api_instance.operational_webhook_controller_get(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling WebhookEndpointApi->operational_webhook_controller_get: #{e}"
end
```

#### Using the operational_webhook_controller_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<OperationalWebhookEndpointResponseDto>, Integer, Hash)> operational_webhook_controller_get_with_http_info(id)

```ruby
begin
  # Get Operational Webhook Endpoint
  data, status_code, headers = api_instance.operational_webhook_controller_get_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <OperationalWebhookEndpointResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling WebhookEndpointApi->operational_webhook_controller_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The endpoint ID or UID |  |

### Return type

[**OperationalWebhookEndpointResponseDto**](OperationalWebhookEndpointResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## operational_webhook_controller_get_headers

> <OperationalWebhookEndpointHeadersResponseDto> operational_webhook_controller_get_headers(id)

Get Operational Webhook Endpoint Headers

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::WebhookEndpointApi.new
id = 'id_example' # String | The endpoint ID or UID

begin
  # Get Operational Webhook Endpoint Headers
  result = api_instance.operational_webhook_controller_get_headers(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling WebhookEndpointApi->operational_webhook_controller_get_headers: #{e}"
end
```

#### Using the operational_webhook_controller_get_headers_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<OperationalWebhookEndpointHeadersResponseDto>, Integer, Hash)> operational_webhook_controller_get_headers_with_http_info(id)

```ruby
begin
  # Get Operational Webhook Endpoint Headers
  data, status_code, headers = api_instance.operational_webhook_controller_get_headers_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <OperationalWebhookEndpointHeadersResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling WebhookEndpointApi->operational_webhook_controller_get_headers_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The endpoint ID or UID |  |

### Return type

[**OperationalWebhookEndpointHeadersResponseDto**](OperationalWebhookEndpointHeadersResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## operational_webhook_controller_get_secret

> <OperationalWebhookEndpointSecretResponseDto> operational_webhook_controller_get_secret(id)

Get Operational Webhook Endpoint Secret

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::WebhookEndpointApi.new
id = 'id_example' # String | The endpoint ID or UID

begin
  # Get Operational Webhook Endpoint Secret
  result = api_instance.operational_webhook_controller_get_secret(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling WebhookEndpointApi->operational_webhook_controller_get_secret: #{e}"
end
```

#### Using the operational_webhook_controller_get_secret_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<OperationalWebhookEndpointSecretResponseDto>, Integer, Hash)> operational_webhook_controller_get_secret_with_http_info(id)

```ruby
begin
  # Get Operational Webhook Endpoint Secret
  data, status_code, headers = api_instance.operational_webhook_controller_get_secret_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <OperationalWebhookEndpointSecretResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling WebhookEndpointApi->operational_webhook_controller_get_secret_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The endpoint ID or UID |  |

### Return type

[**OperationalWebhookEndpointSecretResponseDto**](OperationalWebhookEndpointSecretResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## operational_webhook_controller_list

> <OperationalWebhookEndpointListResponseDto> operational_webhook_controller_list

List Operational Webhook Endpoints

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::WebhookEndpointApi.new

begin
  # List Operational Webhook Endpoints
  result = api_instance.operational_webhook_controller_list
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling WebhookEndpointApi->operational_webhook_controller_list: #{e}"
end
```

#### Using the operational_webhook_controller_list_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<OperationalWebhookEndpointListResponseDto>, Integer, Hash)> operational_webhook_controller_list_with_http_info

```ruby
begin
  # List Operational Webhook Endpoints
  data, status_code, headers = api_instance.operational_webhook_controller_list_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <OperationalWebhookEndpointListResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling WebhookEndpointApi->operational_webhook_controller_list_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**OperationalWebhookEndpointListResponseDto**](OperationalWebhookEndpointListResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## operational_webhook_controller_rotate_secret

> operational_webhook_controller_rotate_secret(id, operational_webhook_endpoint_secret_in_dto)

Rotate Operational Webhook Endpoint Secret

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::WebhookEndpointApi.new
id = 'id_example' # String | The endpoint ID or UID
operational_webhook_endpoint_secret_in_dto = Solifyn::OperationalWebhookEndpointSecretInDto.new # OperationalWebhookEndpointSecretInDto | 

begin
  # Rotate Operational Webhook Endpoint Secret
  api_instance.operational_webhook_controller_rotate_secret(id, operational_webhook_endpoint_secret_in_dto)
rescue Solifyn::ApiError => e
  puts "Error when calling WebhookEndpointApi->operational_webhook_controller_rotate_secret: #{e}"
end
```

#### Using the operational_webhook_controller_rotate_secret_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> operational_webhook_controller_rotate_secret_with_http_info(id, operational_webhook_endpoint_secret_in_dto)

```ruby
begin
  # Rotate Operational Webhook Endpoint Secret
  data, status_code, headers = api_instance.operational_webhook_controller_rotate_secret_with_http_info(id, operational_webhook_endpoint_secret_in_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling WebhookEndpointApi->operational_webhook_controller_rotate_secret_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The endpoint ID or UID |  |
| **operational_webhook_endpoint_secret_in_dto** | [**OperationalWebhookEndpointSecretInDto**](OperationalWebhookEndpointSecretInDto.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## operational_webhook_controller_update

> <OperationalWebhookEndpointResponseDto> operational_webhook_controller_update(id, operational_webhook_endpoint_update_dto)

Update Operational Webhook Endpoint

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::WebhookEndpointApi.new
id = 'id_example' # String | The endpoint ID or UID
operational_webhook_endpoint_update_dto = Solifyn::OperationalWebhookEndpointUpdateDto.new({url: 'https://example.com/new-webhook/'}) # OperationalWebhookEndpointUpdateDto | 

begin
  # Update Operational Webhook Endpoint
  result = api_instance.operational_webhook_controller_update(id, operational_webhook_endpoint_update_dto)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling WebhookEndpointApi->operational_webhook_controller_update: #{e}"
end
```

#### Using the operational_webhook_controller_update_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<OperationalWebhookEndpointResponseDto>, Integer, Hash)> operational_webhook_controller_update_with_http_info(id, operational_webhook_endpoint_update_dto)

```ruby
begin
  # Update Operational Webhook Endpoint
  data, status_code, headers = api_instance.operational_webhook_controller_update_with_http_info(id, operational_webhook_endpoint_update_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <OperationalWebhookEndpointResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling WebhookEndpointApi->operational_webhook_controller_update_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The endpoint ID or UID |  |
| **operational_webhook_endpoint_update_dto** | [**OperationalWebhookEndpointUpdateDto**](OperationalWebhookEndpointUpdateDto.md) |  |  |

### Return type

[**OperationalWebhookEndpointResponseDto**](OperationalWebhookEndpointResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## operational_webhook_controller_update_headers

> operational_webhook_controller_update_headers(id, operational_webhook_endpoint_headers_in_dto)

Set Operational Webhook Endpoint Headers

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::WebhookEndpointApi.new
id = 'id_example' # String | The endpoint ID or UID
operational_webhook_endpoint_headers_in_dto = Solifyn::OperationalWebhookEndpointHeadersInDto.new({headers: {"X-Example":"123","X-Foobar":"Bar"}}) # OperationalWebhookEndpointHeadersInDto | 

begin
  # Set Operational Webhook Endpoint Headers
  api_instance.operational_webhook_controller_update_headers(id, operational_webhook_endpoint_headers_in_dto)
rescue Solifyn::ApiError => e
  puts "Error when calling WebhookEndpointApi->operational_webhook_controller_update_headers: #{e}"
end
```

#### Using the operational_webhook_controller_update_headers_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> operational_webhook_controller_update_headers_with_http_info(id, operational_webhook_endpoint_headers_in_dto)

```ruby
begin
  # Set Operational Webhook Endpoint Headers
  data, status_code, headers = api_instance.operational_webhook_controller_update_headers_with_http_info(id, operational_webhook_endpoint_headers_in_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling WebhookEndpointApi->operational_webhook_controller_update_headers_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The endpoint ID or UID |  |
| **operational_webhook_endpoint_headers_in_dto** | [**OperationalWebhookEndpointHeadersInDto**](OperationalWebhookEndpointHeadersInDto.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

