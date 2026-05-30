# Solifyn::BillingApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**billing_get_plans**](BillingApi.md#billing_get_plans) | **GET** /v1/billing/plans | Get Platform Plans |


## billing_get_plans

> billing_get_plans

Get Platform Plans

Returns all available platform subscription plans with fees and features.

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::BillingApi.new

begin
  # Get Platform Plans
  api_instance.billing_get_plans
rescue Solifyn::ApiError => e
  puts "Error when calling BillingApi->billing_get_plans: #{e}"
end
```

#### Using the billing_get_plans_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> billing_get_plans_with_http_info

```ruby
begin
  # Get Platform Plans
  data, status_code, headers = api_instance.billing_get_plans_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling BillingApi->billing_get_plans_with_http_info: #{e}"
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

