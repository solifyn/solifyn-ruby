# Solifyn::DeveloperApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**developer_controller_create_api_key**](DeveloperApi.md#developer_controller_create_api_key) | **POST** /v1/developer/api-keys |  |
| [**developer_controller_create_webhook_endpoint**](DeveloperApi.md#developer_controller_create_webhook_endpoint) | **POST** /v1/developer/webhooks |  |
| [**developer_controller_delete_api_key**](DeveloperApi.md#developer_controller_delete_api_key) | **DELETE** /v1/developer/api-keys/{id} |  |
| [**developer_controller_delete_webhook_endpoint**](DeveloperApi.md#developer_controller_delete_webhook_endpoint) | **DELETE** /v1/developer/webhooks/{id} |  |
| [**developer_controller_get_api_keys**](DeveloperApi.md#developer_controller_get_api_keys) | **GET** /v1/developer/api-keys |  |
| [**developer_controller_get_app_portal_url**](DeveloperApi.md#developer_controller_get_app_portal_url) | **GET** /v1/developer/webhooks/app-portal |  |
| [**developer_controller_get_webhook_deliveries**](DeveloperApi.md#developer_controller_get_webhook_deliveries) | **GET** /v1/developer/webhooks/{id}/deliveries |  |
| [**developer_controller_get_webhook_endpoints**](DeveloperApi.md#developer_controller_get_webhook_endpoints) | **GET** /v1/developer/webhooks |  |
| [**developer_controller_update_webhook_endpoint**](DeveloperApi.md#developer_controller_update_webhook_endpoint) | **PATCH** /v1/developer/webhooks/{id} |  |


## developer_controller_create_api_key

> developer_controller_create_api_key



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::DeveloperApi.new

begin
  
  api_instance.developer_controller_create_api_key
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_controller_create_api_key: #{e}"
end
```

#### Using the developer_controller_create_api_key_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> developer_controller_create_api_key_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.developer_controller_create_api_key_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_controller_create_api_key_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## developer_controller_create_webhook_endpoint

> developer_controller_create_webhook_endpoint



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::DeveloperApi.new

begin
  
  api_instance.developer_controller_create_webhook_endpoint
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_controller_create_webhook_endpoint: #{e}"
end
```

#### Using the developer_controller_create_webhook_endpoint_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> developer_controller_create_webhook_endpoint_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.developer_controller_create_webhook_endpoint_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_controller_create_webhook_endpoint_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## developer_controller_delete_api_key

> developer_controller_delete_api_key(id)



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::DeveloperApi.new
id = 'id_example' # String | 

begin
  
  api_instance.developer_controller_delete_api_key(id)
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_controller_delete_api_key: #{e}"
end
```

#### Using the developer_controller_delete_api_key_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> developer_controller_delete_api_key_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.developer_controller_delete_api_key_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_controller_delete_api_key_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## developer_controller_delete_webhook_endpoint

> developer_controller_delete_webhook_endpoint(id)



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::DeveloperApi.new
id = 'id_example' # String | 

begin
  
  api_instance.developer_controller_delete_webhook_endpoint(id)
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_controller_delete_webhook_endpoint: #{e}"
end
```

#### Using the developer_controller_delete_webhook_endpoint_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> developer_controller_delete_webhook_endpoint_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.developer_controller_delete_webhook_endpoint_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_controller_delete_webhook_endpoint_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## developer_controller_get_api_keys

> developer_controller_get_api_keys



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::DeveloperApi.new

begin
  
  api_instance.developer_controller_get_api_keys
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_controller_get_api_keys: #{e}"
end
```

#### Using the developer_controller_get_api_keys_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> developer_controller_get_api_keys_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.developer_controller_get_api_keys_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_controller_get_api_keys_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## developer_controller_get_app_portal_url

> developer_controller_get_app_portal_url



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::DeveloperApi.new

begin
  
  api_instance.developer_controller_get_app_portal_url
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_controller_get_app_portal_url: #{e}"
end
```

#### Using the developer_controller_get_app_portal_url_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> developer_controller_get_app_portal_url_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.developer_controller_get_app_portal_url_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_controller_get_app_portal_url_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## developer_controller_get_webhook_deliveries

> developer_controller_get_webhook_deliveries(id)



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::DeveloperApi.new
id = 'id_example' # String | 

begin
  
  api_instance.developer_controller_get_webhook_deliveries(id)
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_controller_get_webhook_deliveries: #{e}"
end
```

#### Using the developer_controller_get_webhook_deliveries_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> developer_controller_get_webhook_deliveries_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.developer_controller_get_webhook_deliveries_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_controller_get_webhook_deliveries_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## developer_controller_get_webhook_endpoints

> developer_controller_get_webhook_endpoints



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::DeveloperApi.new

begin
  
  api_instance.developer_controller_get_webhook_endpoints
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_controller_get_webhook_endpoints: #{e}"
end
```

#### Using the developer_controller_get_webhook_endpoints_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> developer_controller_get_webhook_endpoints_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.developer_controller_get_webhook_endpoints_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_controller_get_webhook_endpoints_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## developer_controller_update_webhook_endpoint

> developer_controller_update_webhook_endpoint(id)



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::DeveloperApi.new
id = 'id_example' # String | 

begin
  
  api_instance.developer_controller_update_webhook_endpoint(id)
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_controller_update_webhook_endpoint: #{e}"
end
```

#### Using the developer_controller_update_webhook_endpoint_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> developer_controller_update_webhook_endpoint_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.developer_controller_update_webhook_endpoint_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DeveloperApi->developer_controller_update_webhook_endpoint_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

