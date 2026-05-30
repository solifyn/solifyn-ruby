# Solifyn::AffiliateApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**affiliate_controller_approve_connection**](AffiliateApi.md#affiliate_controller_approve_connection) | **POST** /v1/affiliate/program/connections/{id}/approve |  |
| [**affiliate_controller_archive_connection**](AffiliateApi.md#affiliate_controller_archive_connection) | **POST** /v1/affiliate/program/connections/{id}/archive |  |
| [**affiliate_controller_delete_override**](AffiliateApi.md#affiliate_controller_delete_override) | **DELETE** /v1/affiliate/program/override/{id} |  |
| [**affiliate_controller_get_earnings_connections**](AffiliateApi.md#affiliate_controller_get_earnings_connections) | **GET** /v1/affiliate/earnings/connections |  |
| [**affiliate_controller_get_earnings_ledger**](AffiliateApi.md#affiliate_controller_get_earnings_ledger) | **GET** /v1/affiliate/earnings/ledger |  |
| [**affiliate_controller_get_earnings_stats**](AffiliateApi.md#affiliate_controller_get_earnings_stats) | **GET** /v1/affiliate/earnings/stats |  |
| [**affiliate_controller_get_marketplace**](AffiliateApi.md#affiliate_controller_get_marketplace) | **GET** /v1/affiliate/marketplace |  |
| [**affiliate_controller_get_program_connections**](AffiliateApi.md#affiliate_controller_get_program_connections) | **GET** /v1/affiliate/program/connections |  |
| [**affiliate_controller_get_program_ledger**](AffiliateApi.md#affiliate_controller_get_program_ledger) | **GET** /v1/affiliate/program/ledger |  |
| [**affiliate_controller_get_program_settings**](AffiliateApi.md#affiliate_controller_get_program_settings) | **GET** /v1/affiliate/program/settings |  |
| [**affiliate_controller_join_program**](AffiliateApi.md#affiliate_controller_join_program) | **POST** /v1/affiliate/marketplace/join |  |
| [**affiliate_controller_reject_connection**](AffiliateApi.md#affiliate_controller_reject_connection) | **POST** /v1/affiliate/program/connections/{id}/reject |  |
| [**affiliate_controller_save_override**](AffiliateApi.md#affiliate_controller_save_override) | **POST** /v1/affiliate/program/override |  |
| [**affiliate_controller_save_program_settings**](AffiliateApi.md#affiliate_controller_save_program_settings) | **POST** /v1/affiliate/program/settings |  |


## affiliate_controller_approve_connection

> affiliate_controller_approve_connection(id)



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::AffiliateApi.new
id = 'id_example' # String | 

begin
  
  api_instance.affiliate_controller_approve_connection(id)
rescue Solifyn::ApiError => e
  puts "Error when calling AffiliateApi->affiliate_controller_approve_connection: #{e}"
end
```

#### Using the affiliate_controller_approve_connection_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> affiliate_controller_approve_connection_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.affiliate_controller_approve_connection_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling AffiliateApi->affiliate_controller_approve_connection_with_http_info: #{e}"
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


## affiliate_controller_archive_connection

> affiliate_controller_archive_connection(id)



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::AffiliateApi.new
id = 'id_example' # String | 

begin
  
  api_instance.affiliate_controller_archive_connection(id)
rescue Solifyn::ApiError => e
  puts "Error when calling AffiliateApi->affiliate_controller_archive_connection: #{e}"
end
```

#### Using the affiliate_controller_archive_connection_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> affiliate_controller_archive_connection_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.affiliate_controller_archive_connection_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling AffiliateApi->affiliate_controller_archive_connection_with_http_info: #{e}"
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


## affiliate_controller_delete_override

> affiliate_controller_delete_override(id)



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::AffiliateApi.new
id = 'id_example' # String | 

begin
  
  api_instance.affiliate_controller_delete_override(id)
rescue Solifyn::ApiError => e
  puts "Error when calling AffiliateApi->affiliate_controller_delete_override: #{e}"
end
```

#### Using the affiliate_controller_delete_override_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> affiliate_controller_delete_override_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.affiliate_controller_delete_override_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling AffiliateApi->affiliate_controller_delete_override_with_http_info: #{e}"
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


## affiliate_controller_get_earnings_connections

> affiliate_controller_get_earnings_connections



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::AffiliateApi.new

begin
  
  api_instance.affiliate_controller_get_earnings_connections
rescue Solifyn::ApiError => e
  puts "Error when calling AffiliateApi->affiliate_controller_get_earnings_connections: #{e}"
end
```

#### Using the affiliate_controller_get_earnings_connections_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> affiliate_controller_get_earnings_connections_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.affiliate_controller_get_earnings_connections_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling AffiliateApi->affiliate_controller_get_earnings_connections_with_http_info: #{e}"
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


## affiliate_controller_get_earnings_ledger

> affiliate_controller_get_earnings_ledger



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::AffiliateApi.new

begin
  
  api_instance.affiliate_controller_get_earnings_ledger
rescue Solifyn::ApiError => e
  puts "Error when calling AffiliateApi->affiliate_controller_get_earnings_ledger: #{e}"
end
```

#### Using the affiliate_controller_get_earnings_ledger_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> affiliate_controller_get_earnings_ledger_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.affiliate_controller_get_earnings_ledger_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling AffiliateApi->affiliate_controller_get_earnings_ledger_with_http_info: #{e}"
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


## affiliate_controller_get_earnings_stats

> affiliate_controller_get_earnings_stats



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::AffiliateApi.new

begin
  
  api_instance.affiliate_controller_get_earnings_stats
rescue Solifyn::ApiError => e
  puts "Error when calling AffiliateApi->affiliate_controller_get_earnings_stats: #{e}"
end
```

#### Using the affiliate_controller_get_earnings_stats_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> affiliate_controller_get_earnings_stats_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.affiliate_controller_get_earnings_stats_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling AffiliateApi->affiliate_controller_get_earnings_stats_with_http_info: #{e}"
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


## affiliate_controller_get_marketplace

> affiliate_controller_get_marketplace



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::AffiliateApi.new

begin
  
  api_instance.affiliate_controller_get_marketplace
rescue Solifyn::ApiError => e
  puts "Error when calling AffiliateApi->affiliate_controller_get_marketplace: #{e}"
end
```

#### Using the affiliate_controller_get_marketplace_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> affiliate_controller_get_marketplace_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.affiliate_controller_get_marketplace_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling AffiliateApi->affiliate_controller_get_marketplace_with_http_info: #{e}"
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


## affiliate_controller_get_program_connections

> affiliate_controller_get_program_connections



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::AffiliateApi.new

begin
  
  api_instance.affiliate_controller_get_program_connections
rescue Solifyn::ApiError => e
  puts "Error when calling AffiliateApi->affiliate_controller_get_program_connections: #{e}"
end
```

#### Using the affiliate_controller_get_program_connections_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> affiliate_controller_get_program_connections_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.affiliate_controller_get_program_connections_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling AffiliateApi->affiliate_controller_get_program_connections_with_http_info: #{e}"
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


## affiliate_controller_get_program_ledger

> affiliate_controller_get_program_ledger



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::AffiliateApi.new

begin
  
  api_instance.affiliate_controller_get_program_ledger
rescue Solifyn::ApiError => e
  puts "Error when calling AffiliateApi->affiliate_controller_get_program_ledger: #{e}"
end
```

#### Using the affiliate_controller_get_program_ledger_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> affiliate_controller_get_program_ledger_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.affiliate_controller_get_program_ledger_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling AffiliateApi->affiliate_controller_get_program_ledger_with_http_info: #{e}"
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


## affiliate_controller_get_program_settings

> affiliate_controller_get_program_settings



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::AffiliateApi.new

begin
  
  api_instance.affiliate_controller_get_program_settings
rescue Solifyn::ApiError => e
  puts "Error when calling AffiliateApi->affiliate_controller_get_program_settings: #{e}"
end
```

#### Using the affiliate_controller_get_program_settings_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> affiliate_controller_get_program_settings_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.affiliate_controller_get_program_settings_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling AffiliateApi->affiliate_controller_get_program_settings_with_http_info: #{e}"
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


## affiliate_controller_join_program

> affiliate_controller_join_program



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::AffiliateApi.new

begin
  
  api_instance.affiliate_controller_join_program
rescue Solifyn::ApiError => e
  puts "Error when calling AffiliateApi->affiliate_controller_join_program: #{e}"
end
```

#### Using the affiliate_controller_join_program_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> affiliate_controller_join_program_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.affiliate_controller_join_program_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling AffiliateApi->affiliate_controller_join_program_with_http_info: #{e}"
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


## affiliate_controller_reject_connection

> affiliate_controller_reject_connection(id)



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::AffiliateApi.new
id = 'id_example' # String | 

begin
  
  api_instance.affiliate_controller_reject_connection(id)
rescue Solifyn::ApiError => e
  puts "Error when calling AffiliateApi->affiliate_controller_reject_connection: #{e}"
end
```

#### Using the affiliate_controller_reject_connection_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> affiliate_controller_reject_connection_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.affiliate_controller_reject_connection_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling AffiliateApi->affiliate_controller_reject_connection_with_http_info: #{e}"
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


## affiliate_controller_save_override

> affiliate_controller_save_override



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::AffiliateApi.new

begin
  
  api_instance.affiliate_controller_save_override
rescue Solifyn::ApiError => e
  puts "Error when calling AffiliateApi->affiliate_controller_save_override: #{e}"
end
```

#### Using the affiliate_controller_save_override_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> affiliate_controller_save_override_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.affiliate_controller_save_override_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling AffiliateApi->affiliate_controller_save_override_with_http_info: #{e}"
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


## affiliate_controller_save_program_settings

> affiliate_controller_save_program_settings



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::AffiliateApi.new

begin
  
  api_instance.affiliate_controller_save_program_settings
rescue Solifyn::ApiError => e
  puts "Error when calling AffiliateApi->affiliate_controller_save_program_settings: #{e}"
end
```

#### Using the affiliate_controller_save_program_settings_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> affiliate_controller_save_program_settings_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.affiliate_controller_save_program_settings_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling AffiliateApi->affiliate_controller_save_program_settings_with_http_info: #{e}"
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

