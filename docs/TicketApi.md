# Solifyn::TicketApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**ticket_controller_create_ticket**](TicketApi.md#ticket_controller_create_ticket) | **POST** /v1/tickets |  |
| [**ticket_controller_get_ticket_details**](TicketApi.md#ticket_controller_get_ticket_details) | **GET** /v1/tickets/{id} |  |
| [**ticket_controller_get_tickets**](TicketApi.md#ticket_controller_get_tickets) | **GET** /v1/tickets |  |
| [**ticket_controller_reply_ticket**](TicketApi.md#ticket_controller_reply_ticket) | **POST** /v1/tickets/{id}/replies |  |
| [**ticket_controller_update_ticket**](TicketApi.md#ticket_controller_update_ticket) | **PATCH** /v1/tickets/{id} |  |


## ticket_controller_create_ticket

> ticket_controller_create_ticket(body)



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::TicketApi.new
body = { ... } # Object | 

begin
  
  api_instance.ticket_controller_create_ticket(body)
rescue Solifyn::ApiError => e
  puts "Error when calling TicketApi->ticket_controller_create_ticket: #{e}"
end
```

#### Using the ticket_controller_create_ticket_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> ticket_controller_create_ticket_with_http_info(body)

```ruby
begin
  
  data, status_code, headers = api_instance.ticket_controller_create_ticket_with_http_info(body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling TicketApi->ticket_controller_create_ticket_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **body** | **Object** |  |  |

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## ticket_controller_get_ticket_details

> ticket_controller_get_ticket_details(id)



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::TicketApi.new
id = 'id_example' # String | 

begin
  
  api_instance.ticket_controller_get_ticket_details(id)
rescue Solifyn::ApiError => e
  puts "Error when calling TicketApi->ticket_controller_get_ticket_details: #{e}"
end
```

#### Using the ticket_controller_get_ticket_details_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> ticket_controller_get_ticket_details_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.ticket_controller_get_ticket_details_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling TicketApi->ticket_controller_get_ticket_details_with_http_info: #{e}"
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


## ticket_controller_get_tickets

> ticket_controller_get_tickets



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::TicketApi.new

begin
  
  api_instance.ticket_controller_get_tickets
rescue Solifyn::ApiError => e
  puts "Error when calling TicketApi->ticket_controller_get_tickets: #{e}"
end
```

#### Using the ticket_controller_get_tickets_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> ticket_controller_get_tickets_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.ticket_controller_get_tickets_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling TicketApi->ticket_controller_get_tickets_with_http_info: #{e}"
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


## ticket_controller_reply_ticket

> ticket_controller_reply_ticket(id, body)



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::TicketApi.new
id = 'id_example' # String | 
body = { ... } # Object | 

begin
  
  api_instance.ticket_controller_reply_ticket(id, body)
rescue Solifyn::ApiError => e
  puts "Error when calling TicketApi->ticket_controller_reply_ticket: #{e}"
end
```

#### Using the ticket_controller_reply_ticket_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> ticket_controller_reply_ticket_with_http_info(id, body)

```ruby
begin
  
  data, status_code, headers = api_instance.ticket_controller_reply_ticket_with_http_info(id, body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling TicketApi->ticket_controller_reply_ticket_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **body** | **Object** |  |  |

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## ticket_controller_update_ticket

> ticket_controller_update_ticket(id, body)



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::TicketApi.new
id = 'id_example' # String | 
body = { ... } # Object | 

begin
  
  api_instance.ticket_controller_update_ticket(id, body)
rescue Solifyn::ApiError => e
  puts "Error when calling TicketApi->ticket_controller_update_ticket: #{e}"
end
```

#### Using the ticket_controller_update_ticket_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> ticket_controller_update_ticket_with_http_info(id, body)

```ruby
begin
  
  data, status_code, headers = api_instance.ticket_controller_update_ticket_with_http_info(id, body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling TicketApi->ticket_controller_update_ticket_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **body** | **Object** |  |  |

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

