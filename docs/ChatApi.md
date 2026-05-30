# Solifyn::ChatApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**chat_controller_get_merchant_messages**](ChatApi.md#chat_controller_get_merchant_messages) | **GET** /v1/chat/merchant/messages/{customerId} |  |
| [**chat_controller_get_merchant_sessions**](ChatApi.md#chat_controller_get_merchant_sessions) | **GET** /v1/chat/merchant/sessions |  |
| [**chat_controller_send_customer_message**](ChatApi.md#chat_controller_send_customer_message) | **POST** /v1/chat/customer/message |  |
| [**chat_controller_send_merchant_message**](ChatApi.md#chat_controller_send_merchant_message) | **POST** /v1/chat/merchant/message |  |


## chat_controller_get_merchant_messages

> chat_controller_get_merchant_messages(customer_id)



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::ChatApi.new
customer_id = 'customer_id_example' # String | 

begin
  
  api_instance.chat_controller_get_merchant_messages(customer_id)
rescue Solifyn::ApiError => e
  puts "Error when calling ChatApi->chat_controller_get_merchant_messages: #{e}"
end
```

#### Using the chat_controller_get_merchant_messages_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> chat_controller_get_merchant_messages_with_http_info(customer_id)

```ruby
begin
  
  data, status_code, headers = api_instance.chat_controller_get_merchant_messages_with_http_info(customer_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling ChatApi->chat_controller_get_merchant_messages_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## chat_controller_get_merchant_sessions

> chat_controller_get_merchant_sessions



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::ChatApi.new

begin
  
  api_instance.chat_controller_get_merchant_sessions
rescue Solifyn::ApiError => e
  puts "Error when calling ChatApi->chat_controller_get_merchant_sessions: #{e}"
end
```

#### Using the chat_controller_get_merchant_sessions_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> chat_controller_get_merchant_sessions_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.chat_controller_get_merchant_sessions_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling ChatApi->chat_controller_get_merchant_sessions_with_http_info: #{e}"
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


## chat_controller_send_customer_message

> chat_controller_send_customer_message



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::ChatApi.new

begin
  
  api_instance.chat_controller_send_customer_message
rescue Solifyn::ApiError => e
  puts "Error when calling ChatApi->chat_controller_send_customer_message: #{e}"
end
```

#### Using the chat_controller_send_customer_message_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> chat_controller_send_customer_message_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.chat_controller_send_customer_message_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling ChatApi->chat_controller_send_customer_message_with_http_info: #{e}"
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


## chat_controller_send_merchant_message

> chat_controller_send_merchant_message



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::ChatApi.new

begin
  
  api_instance.chat_controller_send_merchant_message
rescue Solifyn::ApiError => e
  puts "Error when calling ChatApi->chat_controller_send_merchant_message: #{e}"
end
```

#### Using the chat_controller_send_merchant_message_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> chat_controller_send_merchant_message_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.chat_controller_send_merchant_message_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling ChatApi->chat_controller_send_merchant_message_with_http_info: #{e}"
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

