# Solifyn::BalanceApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**balance_controller_find_all**](BalanceApi.md#balance_controller_find_all) | **GET** /v1/balances |  |
| [**balance_controller_generate_report**](BalanceApi.md#balance_controller_generate_report) | **GET** /v1/balances/report |  |
| [**balance_controller_get_summary**](BalanceApi.md#balance_controller_get_summary) | **GET** /v1/balances/summary |  |


## balance_controller_find_all

> balance_controller_find_all



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::BalanceApi.new

begin
  
  api_instance.balance_controller_find_all
rescue Solifyn::ApiError => e
  puts "Error when calling BalanceApi->balance_controller_find_all: #{e}"
end
```

#### Using the balance_controller_find_all_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> balance_controller_find_all_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.balance_controller_find_all_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling BalanceApi->balance_controller_find_all_with_http_info: #{e}"
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


## balance_controller_generate_report

> balance_controller_generate_report



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::BalanceApi.new

begin
  
  api_instance.balance_controller_generate_report
rescue Solifyn::ApiError => e
  puts "Error when calling BalanceApi->balance_controller_generate_report: #{e}"
end
```

#### Using the balance_controller_generate_report_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> balance_controller_generate_report_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.balance_controller_generate_report_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling BalanceApi->balance_controller_generate_report_with_http_info: #{e}"
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


## balance_controller_get_summary

> balance_controller_get_summary



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::BalanceApi.new

begin
  
  api_instance.balance_controller_get_summary
rescue Solifyn::ApiError => e
  puts "Error when calling BalanceApi->balance_controller_get_summary: #{e}"
end
```

#### Using the balance_controller_get_summary_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> balance_controller_get_summary_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.balance_controller_get_summary_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling BalanceApi->balance_controller_get_summary_with_http_info: #{e}"
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

