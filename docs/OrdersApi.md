# Solifyn::OrdersApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**orders_get**](OrdersApi.md#orders_get) | **GET** /v1/orders/{id} | Retrieve Order |
| [**orders_get_invoice**](OrdersApi.md#orders_get_invoice) | **GET** /v1/orders/{id}/invoice | Get Order Invoice |
| [**orders_list**](OrdersApi.md#orders_list) | **GET** /v1/orders | List Orders |
| [**orders_update**](OrdersApi.md#orders_update) | **PATCH** /v1/orders/{id} | Update Order Billing Address |
| [**refunds_create**](OrdersApi.md#refunds_create) | **POST** /v1/orders/{id}/refund | Create Refund |


## orders_get

> <Order> orders_get(id)

Retrieve Order

Retrieve details of a specific order/payment by ID.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::OrdersApi.new
id = 'pay_123' # String | The unique order/payment ID.

begin
  # Retrieve Order
  result = api_instance.orders_get(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling OrdersApi->orders_get: #{e}"
end
```

#### Using the orders_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Order>, Integer, Hash)> orders_get_with_http_info(id)

```ruby
begin
  # Retrieve Order
  data, status_code, headers = api_instance.orders_get_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Order>
rescue Solifyn::ApiError => e
  puts "Error when calling OrdersApi->orders_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique order/payment ID. |  |

### Return type

[**Order**](Order.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## orders_get_invoice

> <Invoice> orders_get_invoice(id)

Get Order Invoice

Retrieve the generated invoice details for the specified order.

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::OrdersApi.new
id = 'pay_123' # String | The unique order/payment ID.

begin
  # Get Order Invoice
  result = api_instance.orders_get_invoice(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling OrdersApi->orders_get_invoice: #{e}"
end
```

#### Using the orders_get_invoice_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Invoice>, Integer, Hash)> orders_get_invoice_with_http_info(id)

```ruby
begin
  # Get Order Invoice
  data, status_code, headers = api_instance.orders_get_invoice_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Invoice>
rescue Solifyn::ApiError => e
  puts "Error when calling OrdersApi->orders_get_invoice_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique order/payment ID. |  |

### Return type

[**Invoice**](Invoice.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## orders_list

> <OrderList> orders_list(opts)

List Orders

List and query orders/payments belonging to your active business.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::OrdersApi.new
opts = {
  created_at_lte: 'created_at_lte_example', # String | Filter by creation date less than or equal to.
  created_at_gte: 'created_at_gte_example', # String | Filter by creation date greater than or equal to.
  product_id: 'product_id_example', # String | Filter by product identifier.
  customer_id: 'customer_id_example', # String | Filter by customer identifier.
  status: 'status_example', # String | Filter by order/payment status.
  page_size: 8.14, # Float | Size of a page, defaults to 10. Maximum is 100.
  page_number: 8.14 # Float | Page number, defaults to 1.
}

begin
  # List Orders
  result = api_instance.orders_list(opts)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling OrdersApi->orders_list: #{e}"
end
```

#### Using the orders_list_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<OrderList>, Integer, Hash)> orders_list_with_http_info(opts)

```ruby
begin
  # List Orders
  data, status_code, headers = api_instance.orders_list_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <OrderList>
rescue Solifyn::ApiError => e
  puts "Error when calling OrdersApi->orders_list_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **created_at_lte** | **String** | Filter by creation date less than or equal to. | [optional] |
| **created_at_gte** | **String** | Filter by creation date greater than or equal to. | [optional] |
| **product_id** | **String** | Filter by product identifier. | [optional] |
| **customer_id** | **String** | Filter by customer identifier. | [optional] |
| **status** | **String** | Filter by order/payment status. | [optional] |
| **page_size** | **Float** | Size of a page, defaults to 10. Maximum is 100. | [optional][default to 10] |
| **page_number** | **Float** | Page number, defaults to 1. | [optional][default to 1] |

### Return type

[**OrderList**](OrderList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## orders_update

> <Order> orders_update(id, order_update)

Update Order Billing Address

Update the billing details of an existing order.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::OrdersApi.new
id = 'pay_123' # String | The unique order/payment ID.
order_update = Solifyn::OrderUpdate.new # OrderUpdate | 

begin
  # Update Order Billing Address
  result = api_instance.orders_update(id, order_update)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling OrdersApi->orders_update: #{e}"
end
```

#### Using the orders_update_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Order>, Integer, Hash)> orders_update_with_http_info(id, order_update)

```ruby
begin
  # Update Order Billing Address
  data, status_code, headers = api_instance.orders_update_with_http_info(id, order_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Order>
rescue Solifyn::ApiError => e
  puts "Error when calling OrdersApi->orders_update_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique order/payment ID. |  |
| **order_update** | [**OrderUpdate**](OrderUpdate.md) |  |  |

### Return type

[**Order**](Order.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


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

api_instance = Solifyn::OrdersApi.new
id = 'pay_123' # String | The unique order/payment ID.
order_refund_create = Solifyn::OrderRefundCreate.new({amount: 1000, is_full_refund: true, idempotency_key: 'ref_idem_98sdufhskjfsd'}) # OrderRefundCreate | 

begin
  # Create Refund
  api_instance.refunds_create(id, order_refund_create)
rescue Solifyn::ApiError => e
  puts "Error when calling OrdersApi->refunds_create: #{e}"
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
  puts "Error when calling OrdersApi->refunds_create_with_http_info: #{e}"
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

