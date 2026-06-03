# Solifyn::RefundRequestsApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**refund_requests_list**](RefundRequestsApi.md#refund_requests_list) | **GET** /v1/refund-requests | List Refund Requests (Merchant) |
| [**refund_requests_list_messages**](RefundRequestsApi.md#refund_requests_list_messages) | **GET** /v1/refund-requests/{id}/messages | List Messages for Refund Request (Merchant) |
| [**refund_requests_send_message**](RefundRequestsApi.md#refund_requests_send_message) | **POST** /v1/refund-requests/{id}/messages | Send Refund Request Message (Merchant) |
| [**refund_requests_update_status**](RefundRequestsApi.md#refund_requests_update_status) | **PATCH** /v1/refund-requests/{id}/status | Update Refund Request Status (Merchant) |
| [**refund_requests_upload_evidence**](RefundRequestsApi.md#refund_requests_upload_evidence) | **POST** /v1/refund-requests/upload-evidence | Upload Dispute Evidence File (Merchant) |


## refund_requests_list

> refund_requests_list

List Refund Requests (Merchant)

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::RefundRequestsApi.new

begin
  # List Refund Requests (Merchant)
  api_instance.refund_requests_list
rescue Solifyn::ApiError => e
  puts "Error when calling RefundRequestsApi->refund_requests_list: #{e}"
end
```

#### Using the refund_requests_list_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> refund_requests_list_with_http_info

```ruby
begin
  # List Refund Requests (Merchant)
  data, status_code, headers = api_instance.refund_requests_list_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling RefundRequestsApi->refund_requests_list_with_http_info: #{e}"
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


## refund_requests_list_messages

> refund_requests_list_messages(id)

List Messages for Refund Request (Merchant)

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::RefundRequestsApi.new
id = 'id_example' # String | 

begin
  # List Messages for Refund Request (Merchant)
  api_instance.refund_requests_list_messages(id)
rescue Solifyn::ApiError => e
  puts "Error when calling RefundRequestsApi->refund_requests_list_messages: #{e}"
end
```

#### Using the refund_requests_list_messages_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> refund_requests_list_messages_with_http_info(id)

```ruby
begin
  # List Messages for Refund Request (Merchant)
  data, status_code, headers = api_instance.refund_requests_list_messages_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling RefundRequestsApi->refund_requests_list_messages_with_http_info: #{e}"
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


## refund_requests_send_message

> refund_requests_send_message(id)

Send Refund Request Message (Merchant)

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::RefundRequestsApi.new
id = 'id_example' # String | 

begin
  # Send Refund Request Message (Merchant)
  api_instance.refund_requests_send_message(id)
rescue Solifyn::ApiError => e
  puts "Error when calling RefundRequestsApi->refund_requests_send_message: #{e}"
end
```

#### Using the refund_requests_send_message_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> refund_requests_send_message_with_http_info(id)

```ruby
begin
  # Send Refund Request Message (Merchant)
  data, status_code, headers = api_instance.refund_requests_send_message_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling RefundRequestsApi->refund_requests_send_message_with_http_info: #{e}"
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


## refund_requests_update_status

> refund_requests_update_status(id)

Update Refund Request Status (Merchant)

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::RefundRequestsApi.new
id = 'id_example' # String | 

begin
  # Update Refund Request Status (Merchant)
  api_instance.refund_requests_update_status(id)
rescue Solifyn::ApiError => e
  puts "Error when calling RefundRequestsApi->refund_requests_update_status: #{e}"
end
```

#### Using the refund_requests_update_status_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> refund_requests_update_status_with_http_info(id)

```ruby
begin
  # Update Refund Request Status (Merchant)
  data, status_code, headers = api_instance.refund_requests_update_status_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling RefundRequestsApi->refund_requests_update_status_with_http_info: #{e}"
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


## refund_requests_upload_evidence

> refund_requests_upload_evidence

Upload Dispute Evidence File (Merchant)

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::RefundRequestsApi.new

begin
  # Upload Dispute Evidence File (Merchant)
  api_instance.refund_requests_upload_evidence
rescue Solifyn::ApiError => e
  puts "Error when calling RefundRequestsApi->refund_requests_upload_evidence: #{e}"
end
```

#### Using the refund_requests_upload_evidence_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> refund_requests_upload_evidence_with_http_info

```ruby
begin
  # Upload Dispute Evidence File (Merchant)
  data, status_code, headers = api_instance.refund_requests_upload_evidence_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling RefundRequestsApi->refund_requests_upload_evidence_with_http_info: #{e}"
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

