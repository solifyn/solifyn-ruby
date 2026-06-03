# Solifyn::DeveloperApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**developer_create_api_key**](DeveloperApi.md#developer_create_api_key) | **POST** /v1/developer/api-keys | Create Developer API Key |
| [**developer_create_webhook**](DeveloperApi.md#developer_create_webhook) | **POST** /v1/developer/webhooks | Create Webhook Endpoint |
| [**developer_delete_webhook**](DeveloperApi.md#developer_delete_webhook) | **DELETE** /v1/developer/webhooks/{id} | Delete Webhook Endpoint |
| [**developer_get_app_portal**](DeveloperApi.md#developer_get_app_portal) | **GET** /v1/developer/webhooks/app-portal | Retrieve Hosted Webhooks Portal URL |
| [**developer_get_webhook**](DeveloperApi.md#developer_get_webhook) | **GET** /v1/developer/webhooks/{id} | Retrieve Webhook Endpoint Details |
| [**developer_list_api_keys**](DeveloperApi.md#developer_list_api_keys) | **GET** /v1/developer/api-keys | List Developer API Keys |
| [**developer_list_webhook_deliveries**](DeveloperApi.md#developer_list_webhook_deliveries) | **GET** /v1/developer/webhooks/{id}/deliveries | Retrieve Webhook Delivery Logs |
| [**developer_list_webhooks**](DeveloperApi.md#developer_list_webhooks) | **GET** /v1/developer/webhooks | List Webhook Endpoints |
| [**developer_revoke_api_key**](DeveloperApi.md#developer_revoke_api_key) | **DELETE** /v1/developer/api-keys/{id} | Revoke API Key |
| [**developer_update_webhook**](DeveloperApi.md#developer_update_webhook) | **PATCH** /v1/developer/webhooks/{id} | Update Webhook Endpoint |


## developer_create_api_key

> <ApiKeyResponseDto> developer_create_api_key(create_api_key_dto)

Create Developer API Key

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::DeveloperApi.new
create_api_key_dto = Solifyn::CreateApiKeyDto.new({name: 'Production Key'}) # CreateApiKeyDto | 

begin
  # Create Developer API Key
  result = api_instance.developer_create_api_key(create_api_key_dto)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_create_api_key: #{e}"
end
```

#### Using the developer_create_api_key_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ApiKeyResponseDto>, Integer, Hash)> developer_create_api_key_with_http_info(create_api_key_dto)

```ruby
begin
  # Create Developer API Key
  data, status_code, headers = api_instance.developer_create_api_key_with_http_info(create_api_key_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ApiKeyResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_create_api_key_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_api_key_dto** | [**CreateApiKeyDto**](CreateApiKeyDto.md) |  |  |

### Return type

[**ApiKeyResponseDto**](ApiKeyResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## developer_create_webhook

> <WebhookEndpointResponseDto> developer_create_webhook(create_webhook_endpoint_dto)

Create Webhook Endpoint

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::DeveloperApi.new
create_webhook_endpoint_dto = Solifyn::CreateWebhookEndpointDto.new({url: 'https://api.example.com/webhooks', events: [payment.created,  payment.succeeded]}) # CreateWebhookEndpointDto | 

begin
  # Create Webhook Endpoint
  result = api_instance.developer_create_webhook(create_webhook_endpoint_dto)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_create_webhook: #{e}"
end
```

#### Using the developer_create_webhook_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WebhookEndpointResponseDto>, Integer, Hash)> developer_create_webhook_with_http_info(create_webhook_endpoint_dto)

```ruby
begin
  # Create Webhook Endpoint
  data, status_code, headers = api_instance.developer_create_webhook_with_http_info(create_webhook_endpoint_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WebhookEndpointResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_create_webhook_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_webhook_endpoint_dto** | [**CreateWebhookEndpointDto**](CreateWebhookEndpointDto.md) |  |  |

### Return type

[**WebhookEndpointResponseDto**](WebhookEndpointResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## developer_delete_webhook

> developer_delete_webhook(id)

Delete Webhook Endpoint

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::DeveloperApi.new
id = 'id_example' # String | The webhook endpoint ID

begin
  # Delete Webhook Endpoint
  api_instance.developer_delete_webhook(id)
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_delete_webhook: #{e}"
end
```

#### Using the developer_delete_webhook_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> developer_delete_webhook_with_http_info(id)

```ruby
begin
  # Delete Webhook Endpoint
  data, status_code, headers = api_instance.developer_delete_webhook_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_delete_webhook_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The webhook endpoint ID |  |

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## developer_get_app_portal

> <AppPortalUrlResponseDto> developer_get_app_portal

Retrieve Hosted Webhooks Portal URL

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::DeveloperApi.new

begin
  # Retrieve Hosted Webhooks Portal URL
  result = api_instance.developer_get_app_portal
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_get_app_portal: #{e}"
end
```

#### Using the developer_get_app_portal_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AppPortalUrlResponseDto>, Integer, Hash)> developer_get_app_portal_with_http_info

```ruby
begin
  # Retrieve Hosted Webhooks Portal URL
  data, status_code, headers = api_instance.developer_get_app_portal_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AppPortalUrlResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_get_app_portal_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**AppPortalUrlResponseDto**](AppPortalUrlResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## developer_get_webhook

> <WebhookEndpointResponseDto> developer_get_webhook(id)

Retrieve Webhook Endpoint Details

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::DeveloperApi.new
id = 'id_example' # String | The webhook endpoint ID

begin
  # Retrieve Webhook Endpoint Details
  result = api_instance.developer_get_webhook(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_get_webhook: #{e}"
end
```

#### Using the developer_get_webhook_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WebhookEndpointResponseDto>, Integer, Hash)> developer_get_webhook_with_http_info(id)

```ruby
begin
  # Retrieve Webhook Endpoint Details
  data, status_code, headers = api_instance.developer_get_webhook_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WebhookEndpointResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_get_webhook_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The webhook endpoint ID |  |

### Return type

[**WebhookEndpointResponseDto**](WebhookEndpointResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## developer_list_api_keys

> <Array<ApiKeyResponseDto>> developer_list_api_keys

List Developer API Keys

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::DeveloperApi.new

begin
  # List Developer API Keys
  result = api_instance.developer_list_api_keys
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_list_api_keys: #{e}"
end
```

#### Using the developer_list_api_keys_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<ApiKeyResponseDto>>, Integer, Hash)> developer_list_api_keys_with_http_info

```ruby
begin
  # List Developer API Keys
  data, status_code, headers = api_instance.developer_list_api_keys_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<ApiKeyResponseDto>>
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_list_api_keys_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;ApiKeyResponseDto&gt;**](ApiKeyResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## developer_list_webhook_deliveries

> <Array<WebhookDeliveryResponseDto>> developer_list_webhook_deliveries(id)

Retrieve Webhook Delivery Logs

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::DeveloperApi.new
id = 'id_example' # String | The webhook endpoint ID

begin
  # Retrieve Webhook Delivery Logs
  result = api_instance.developer_list_webhook_deliveries(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_list_webhook_deliveries: #{e}"
end
```

#### Using the developer_list_webhook_deliveries_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<WebhookDeliveryResponseDto>>, Integer, Hash)> developer_list_webhook_deliveries_with_http_info(id)

```ruby
begin
  # Retrieve Webhook Delivery Logs
  data, status_code, headers = api_instance.developer_list_webhook_deliveries_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<WebhookDeliveryResponseDto>>
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_list_webhook_deliveries_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The webhook endpoint ID |  |

### Return type

[**Array&lt;WebhookDeliveryResponseDto&gt;**](WebhookDeliveryResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## developer_list_webhooks

> <Array<WebhookEndpointResponseDto>> developer_list_webhooks

List Webhook Endpoints

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::DeveloperApi.new

begin
  # List Webhook Endpoints
  result = api_instance.developer_list_webhooks
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_list_webhooks: #{e}"
end
```

#### Using the developer_list_webhooks_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<WebhookEndpointResponseDto>>, Integer, Hash)> developer_list_webhooks_with_http_info

```ruby
begin
  # List Webhook Endpoints
  data, status_code, headers = api_instance.developer_list_webhooks_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<WebhookEndpointResponseDto>>
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_list_webhooks_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;WebhookEndpointResponseDto&gt;**](WebhookEndpointResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## developer_revoke_api_key

> developer_revoke_api_key(id)

Revoke API Key

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::DeveloperApi.new
id = 'id_example' # String | The API key ID

begin
  # Revoke API Key
  api_instance.developer_revoke_api_key(id)
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_revoke_api_key: #{e}"
end
```

#### Using the developer_revoke_api_key_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> developer_revoke_api_key_with_http_info(id)

```ruby
begin
  # Revoke API Key
  data, status_code, headers = api_instance.developer_revoke_api_key_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_revoke_api_key_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The API key ID |  |

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## developer_update_webhook

> <WebhookEndpointResponseDto> developer_update_webhook(id, update_webhook_endpoint_dto)

Update Webhook Endpoint

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::DeveloperApi.new
id = 'id_example' # String | The webhook endpoint ID
update_webhook_endpoint_dto = Solifyn::UpdateWebhookEndpointDto.new # UpdateWebhookEndpointDto | 

begin
  # Update Webhook Endpoint
  result = api_instance.developer_update_webhook(id, update_webhook_endpoint_dto)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_update_webhook: #{e}"
end
```

#### Using the developer_update_webhook_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WebhookEndpointResponseDto>, Integer, Hash)> developer_update_webhook_with_http_info(id, update_webhook_endpoint_dto)

```ruby
begin
  # Update Webhook Endpoint
  data, status_code, headers = api_instance.developer_update_webhook_with_http_info(id, update_webhook_endpoint_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WebhookEndpointResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_update_webhook_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The webhook endpoint ID |  |
| **update_webhook_endpoint_dto** | [**UpdateWebhookEndpointDto**](UpdateWebhookEndpointDto.md) |  |  |

### Return type

[**WebhookEndpointResponseDto**](WebhookEndpointResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

