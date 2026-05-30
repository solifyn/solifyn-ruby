# Solifyn::PartnerApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**partner_controller_get_partner_commissions**](PartnerApi.md#partner_controller_get_partner_commissions) | **GET** /v1/partner/commissions |  |
| [**partner_controller_get_partner_stats**](PartnerApi.md#partner_controller_get_partner_stats) | **GET** /v1/partner/stats |  |


## partner_controller_get_partner_commissions

> partner_controller_get_partner_commissions



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::PartnerApi.new

begin
  
  api_instance.partner_controller_get_partner_commissions
rescue Solifyn::ApiError => e
  puts "Error when calling PartnerApi->partner_controller_get_partner_commissions: #{e}"
end
```

#### Using the partner_controller_get_partner_commissions_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> partner_controller_get_partner_commissions_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.partner_controller_get_partner_commissions_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling PartnerApi->partner_controller_get_partner_commissions_with_http_info: #{e}"
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


## partner_controller_get_partner_stats

> partner_controller_get_partner_stats



### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::PartnerApi.new

begin
  
  api_instance.partner_controller_get_partner_stats
rescue Solifyn::ApiError => e
  puts "Error when calling PartnerApi->partner_controller_get_partner_stats: #{e}"
end
```

#### Using the partner_controller_get_partner_stats_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> partner_controller_get_partner_stats_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.partner_controller_get_partner_stats_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling PartnerApi->partner_controller_get_partner_stats_with_http_info: #{e}"
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

