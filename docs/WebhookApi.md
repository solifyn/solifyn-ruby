# Solifyn::WebhookApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**webhook_controller_handle_svix_webhook**](WebhookApi.md#webhook_controller_handle_svix_webhook) | **POST** /v1/webhook/svix |  |
| [**webhook_controller_handle_webhook**](WebhookApi.md#webhook_controller_handle_webhook) | **POST** /v1/webhook |  |


## webhook_controller_handle_svix_webhook

> webhook_controller_handle_svix_webhook



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::WebhookApi.new

begin
  
  api_instance.webhook_controller_handle_svix_webhook
rescue Solifyn::ApiError => e
  puts "Error when calling WebhookApi->webhook_controller_handle_svix_webhook: #{e}"
end
```

#### Using the webhook_controller_handle_svix_webhook_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> webhook_controller_handle_svix_webhook_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.webhook_controller_handle_svix_webhook_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling WebhookApi->webhook_controller_handle_svix_webhook_with_http_info: #{e}"
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


## webhook_controller_handle_webhook

> webhook_controller_handle_webhook(business_id)



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::WebhookApi.new
business_id = 'business_id_example' # String | 

begin
  
  api_instance.webhook_controller_handle_webhook(business_id)
rescue Solifyn::ApiError => e
  puts "Error when calling WebhookApi->webhook_controller_handle_webhook: #{e}"
end
```

#### Using the webhook_controller_handle_webhook_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> webhook_controller_handle_webhook_with_http_info(business_id)

```ruby
begin
  
  data, status_code, headers = api_instance.webhook_controller_handle_webhook_with_http_info(business_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling WebhookApi->webhook_controller_handle_webhook_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **business_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

