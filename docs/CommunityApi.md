# Solifyn::CommunityApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**community_controller_create_post**](CommunityApi.md#community_controller_create_post) | **POST** /v1/community/posts |  |
| [**community_controller_delete_post**](CommunityApi.md#community_controller_delete_post) | **DELETE** /v1/community/posts/{id} |  |
| [**community_controller_get_posts**](CommunityApi.md#community_controller_get_posts) | **GET** /v1/community/posts |  |
| [**community_controller_like_post**](CommunityApi.md#community_controller_like_post) | **PATCH** /v1/community/posts/{id}/like |  |
| [**community_controller_report_post**](CommunityApi.md#community_controller_report_post) | **POST** /v1/community/posts/{id}/report |  |
| [**community_controller_share_post**](CommunityApi.md#community_controller_share_post) | **PATCH** /v1/community/posts/{id}/share |  |
| [**community_controller_unlike_post**](CommunityApi.md#community_controller_unlike_post) | **PATCH** /v1/community/posts/{id}/unlike |  |
| [**community_controller_update_post**](CommunityApi.md#community_controller_update_post) | **PATCH** /v1/community/posts/{id} |  |


## community_controller_create_post

> community_controller_create_post



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::CommunityApi.new

begin
  
  api_instance.community_controller_create_post
rescue Solifyn::ApiError => e
  puts "Error when calling CommunityApi->community_controller_create_post: #{e}"
end
```

#### Using the community_controller_create_post_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> community_controller_create_post_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.community_controller_create_post_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling CommunityApi->community_controller_create_post_with_http_info: #{e}"
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


## community_controller_delete_post

> community_controller_delete_post(id)



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::CommunityApi.new
id = 'id_example' # String | 

begin
  
  api_instance.community_controller_delete_post(id)
rescue Solifyn::ApiError => e
  puts "Error when calling CommunityApi->community_controller_delete_post: #{e}"
end
```

#### Using the community_controller_delete_post_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> community_controller_delete_post_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.community_controller_delete_post_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling CommunityApi->community_controller_delete_post_with_http_info: #{e}"
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


## community_controller_get_posts

> community_controller_get_posts



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::CommunityApi.new

begin
  
  api_instance.community_controller_get_posts
rescue Solifyn::ApiError => e
  puts "Error when calling CommunityApi->community_controller_get_posts: #{e}"
end
```

#### Using the community_controller_get_posts_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> community_controller_get_posts_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.community_controller_get_posts_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling CommunityApi->community_controller_get_posts_with_http_info: #{e}"
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


## community_controller_like_post

> community_controller_like_post(id)



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::CommunityApi.new
id = 'id_example' # String | 

begin
  
  api_instance.community_controller_like_post(id)
rescue Solifyn::ApiError => e
  puts "Error when calling CommunityApi->community_controller_like_post: #{e}"
end
```

#### Using the community_controller_like_post_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> community_controller_like_post_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.community_controller_like_post_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling CommunityApi->community_controller_like_post_with_http_info: #{e}"
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


## community_controller_report_post

> community_controller_report_post(id)



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::CommunityApi.new
id = 'id_example' # String | 

begin
  
  api_instance.community_controller_report_post(id)
rescue Solifyn::ApiError => e
  puts "Error when calling CommunityApi->community_controller_report_post: #{e}"
end
```

#### Using the community_controller_report_post_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> community_controller_report_post_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.community_controller_report_post_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling CommunityApi->community_controller_report_post_with_http_info: #{e}"
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


## community_controller_share_post

> community_controller_share_post(id)



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::CommunityApi.new
id = 'id_example' # String | 

begin
  
  api_instance.community_controller_share_post(id)
rescue Solifyn::ApiError => e
  puts "Error when calling CommunityApi->community_controller_share_post: #{e}"
end
```

#### Using the community_controller_share_post_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> community_controller_share_post_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.community_controller_share_post_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling CommunityApi->community_controller_share_post_with_http_info: #{e}"
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


## community_controller_unlike_post

> community_controller_unlike_post(id)



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::CommunityApi.new
id = 'id_example' # String | 

begin
  
  api_instance.community_controller_unlike_post(id)
rescue Solifyn::ApiError => e
  puts "Error when calling CommunityApi->community_controller_unlike_post: #{e}"
end
```

#### Using the community_controller_unlike_post_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> community_controller_unlike_post_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.community_controller_unlike_post_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling CommunityApi->community_controller_unlike_post_with_http_info: #{e}"
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


## community_controller_update_post

> community_controller_update_post(id)



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::CommunityApi.new
id = 'id_example' # String | 

begin
  
  api_instance.community_controller_update_post(id)
rescue Solifyn::ApiError => e
  puts "Error when calling CommunityApi->community_controller_update_post: #{e}"
end
```

#### Using the community_controller_update_post_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> community_controller_update_post_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.community_controller_update_post_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling CommunityApi->community_controller_update_post_with_http_info: #{e}"
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

