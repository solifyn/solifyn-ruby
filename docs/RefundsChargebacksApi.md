# Solifyn::RefundsChargebacksApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**refunds_create**](RefundsChargebacksApi.md#refunds_create) | **POST** /v1/orders/{id}/refund | Create Refund |
| [**refunds_get**](RefundsChargebacksApi.md#refunds_get) | **GET** /v1/refunds/{id} | Retrieve Refund details |
| [**refunds_list**](RefundsChargebacksApi.md#refunds_list) | **GET** /v1/refunds | List Refunds |


## refunds_create

> refunds_create(id, order_refund_create)

Create Refund

Initiate a full or partial refund for a specific payment/order.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::RefundsChargebacksApi.new
id = 'pay_123' # String | The unique order/payment ID.
order_refund_create = Solifyn::OrderRefundCreate.new({amount: 1000, is_full_refund: true, idempotency_key: 'ref_idem_98sdufhskjfsd'}) # OrderRefundCreate | 

begin
  # Create Refund
  api_instance.refunds_create(id, order_refund_create)
rescue Solifyn::ApiError => e
  puts "Error when calling RefundsChargebacksApi->refunds_create: #{e}"
end
```

#### Using the refunds_create_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> refunds_create_with_http_info(id, order_refund_create)

```ruby
begin
  # Create Refund
  data, status_code, headers = api_instance.refunds_create_with_http_info(id, order_refund_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling RefundsChargebacksApi->refunds_create_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique order/payment ID. |  |
| **order_refund_create** | [**OrderRefundCreate**](OrderRefundCreate.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## refunds_get

> <Refund> refunds_get(id)

Retrieve Refund details

Get parameters of a specific processed refund by database ID.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::RefundsChargebacksApi.new
id = 'ref_123' # String | Refund ID

begin
  # Retrieve Refund details
  result = api_instance.refunds_get(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling RefundsChargebacksApi->refunds_get: #{e}"
end
```

#### Using the refunds_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Refund>, Integer, Hash)> refunds_get_with_http_info(id)

```ruby
begin
  # Retrieve Refund details
  data, status_code, headers = api_instance.refunds_get_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Refund>
rescue Solifyn::ApiError => e
  puts "Error when calling RefundsChargebacksApi->refunds_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Refund ID |  |

### Return type

[**Refund**](Refund.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## refunds_list

> <Array<Refund>> refunds_list

List Refunds

Retrieve a list of processed refunds and chargeback transactions.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::RefundsChargebacksApi.new

begin
  # List Refunds
  result = api_instance.refunds_list
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling RefundsChargebacksApi->refunds_list: #{e}"
end
```

#### Using the refunds_list_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Refund>>, Integer, Hash)> refunds_list_with_http_info

```ruby
begin
  # List Refunds
  data, status_code, headers = api_instance.refunds_list_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Refund>>
rescue Solifyn::ApiError => e
  puts "Error when calling RefundsChargebacksApi->refunds_list_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;Refund&gt;**](Refund.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

