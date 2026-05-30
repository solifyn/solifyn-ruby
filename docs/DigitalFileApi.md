# Solifyn::DigitalFileApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**digital_file_controller_create**](DigitalFileApi.md#digital_file_controller_create) | **POST** /v1/digital-files |  |
| [**digital_file_controller_find_all**](DigitalFileApi.md#digital_file_controller_find_all) | **GET** /v1/digital-files |  |
| [**digital_file_controller_remove**](DigitalFileApi.md#digital_file_controller_remove) | **DELETE** /v1/digital-files/{id} |  |


## digital_file_controller_create

> digital_file_controller_create



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::DigitalFileApi.new

begin
  
  api_instance.digital_file_controller_create
rescue Solifyn::ApiError => e
  puts "Error when calling DigitalFileApi->digital_file_controller_create: #{e}"
end
```

#### Using the digital_file_controller_create_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> digital_file_controller_create_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.digital_file_controller_create_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DigitalFileApi->digital_file_controller_create_with_http_info: #{e}"
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


## digital_file_controller_find_all

> digital_file_controller_find_all



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::DigitalFileApi.new

begin
  
  api_instance.digital_file_controller_find_all
rescue Solifyn::ApiError => e
  puts "Error when calling DigitalFileApi->digital_file_controller_find_all: #{e}"
end
```

#### Using the digital_file_controller_find_all_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> digital_file_controller_find_all_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.digital_file_controller_find_all_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DigitalFileApi->digital_file_controller_find_all_with_http_info: #{e}"
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


## digital_file_controller_remove

> digital_file_controller_remove(id)



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::DigitalFileApi.new
id = 'id_example' # String | 

begin
  
  api_instance.digital_file_controller_remove(id)
rescue Solifyn::ApiError => e
  puts "Error when calling DigitalFileApi->digital_file_controller_remove: #{e}"
end
```

#### Using the digital_file_controller_remove_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> digital_file_controller_remove_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.digital_file_controller_remove_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DigitalFileApi->digital_file_controller_remove_with_http_info: #{e}"
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

