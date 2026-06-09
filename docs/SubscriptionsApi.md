# Solifyn::SubscriptionsApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**subscriptions_action**](SubscriptionsApi.md#subscriptions_action) | **POST** /v1/subscriptions/{subscriptionId}/{action} | Subscription Action |
| [**subscriptions_get**](SubscriptionsApi.md#subscriptions_get) | **GET** /v1/subscriptions/{id} | Retrieve Subscription Details |
| [**subscriptions_list**](SubscriptionsApi.md#subscriptions_list) | **GET** /v1/subscriptions | List Subscriptions |


## subscriptions_action

> <SubscriptionsAction201Response> subscriptions_action(subscription_id, action, subscription_action)

Subscription Action

Cancel, pause, resume, or add free days to a customer subscription.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::SubscriptionsApi.new
subscription_id = 'mem_123' # String | The customer subscription ID
action = 'add_free_days' # String | The subscription task to execute
subscription_action = Solifyn::SubscriptionAction.new # SubscriptionAction | 

begin
  # Subscription Action
  result = api_instance.subscriptions_action(subscription_id, action, subscription_action)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling SubscriptionsApi->subscriptions_action: #{e}"
end
```

#### Using the subscriptions_action_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SubscriptionsAction201Response>, Integer, Hash)> subscriptions_action_with_http_info(subscription_id, action, subscription_action)

```ruby
begin
  # Subscription Action
  data, status_code, headers = api_instance.subscriptions_action_with_http_info(subscription_id, action, subscription_action)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SubscriptionsAction201Response>
rescue Solifyn::ApiError => e
  puts "Error when calling SubscriptionsApi->subscriptions_action_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **subscription_id** | **String** | The customer subscription ID |  |
| **action** | **String** | The subscription task to execute |  |
| **subscription_action** | [**SubscriptionAction**](SubscriptionAction.md) |  |  |

### Return type

[**SubscriptionsAction201Response**](SubscriptionsAction201Response.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## subscriptions_get

> <SubscriptionDetail> subscriptions_get(id)

Retrieve Subscription Details

Retrieve detailed information about a subscription and its billing history.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::SubscriptionsApi.new
id = 'mem_123' # String | The customer subscription ID

begin
  # Retrieve Subscription Details
  result = api_instance.subscriptions_get(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling SubscriptionsApi->subscriptions_get: #{e}"
end
```

#### Using the subscriptions_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SubscriptionDetail>, Integer, Hash)> subscriptions_get_with_http_info(id)

```ruby
begin
  # Retrieve Subscription Details
  data, status_code, headers = api_instance.subscriptions_get_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SubscriptionDetail>
rescue Solifyn::ApiError => e
  puts "Error when calling SubscriptionsApi->subscriptions_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The customer subscription ID |  |

### Return type

[**SubscriptionDetail**](SubscriptionDetail.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## subscriptions_list

> <SubscriptionList> subscriptions_list(opts)

List Subscriptions

Retrieve a list of customer subscriptions, optionally filtered by customer ID.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::SubscriptionsApi.new
opts = {
  customer_id: 'customer_id_example' # String | Filter subscriptions by customer ID.
}

begin
  # List Subscriptions
  result = api_instance.subscriptions_list(opts)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling SubscriptionsApi->subscriptions_list: #{e}"
end
```

#### Using the subscriptions_list_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SubscriptionList>, Integer, Hash)> subscriptions_list_with_http_info(opts)

```ruby
begin
  # List Subscriptions
  data, status_code, headers = api_instance.subscriptions_list_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SubscriptionList>
rescue Solifyn::ApiError => e
  puts "Error when calling SubscriptionsApi->subscriptions_list_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | Filter subscriptions by customer ID. | [optional] |

### Return type

[**SubscriptionList**](SubscriptionList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

