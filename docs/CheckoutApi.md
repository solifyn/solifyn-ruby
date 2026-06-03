# Solifyn::CheckoutApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**checkout_create**](CheckoutApi.md#checkout_create) | **POST** /v1/checkout/create | Create Checkout Session |
| [**checkout_create_collection**](CheckoutApi.md#checkout_create_collection) | **POST** /v1/checkout/collection/create | Create Collection Checkout Session |
| [**checkout_create_setup**](CheckoutApi.md#checkout_create_setup) | **POST** /v1/checkout/setup-configuration | Create Setup Checkout Configuration |
| [**checkout_get_session**](CheckoutApi.md#checkout_get_session) | **GET** /v1/checkout/session/{id} | Get Checkout Session Details |
| [**checkout_price_preview**](CheckoutApi.md#checkout_price_preview) | **GET** /v1/checkout/price-preview | Get Converted Price Preview |
| [**checkout_supported_currencies**](CheckoutApi.md#checkout_supported_currencies) | **GET** /v1/checkout/supported-currencies | Get Supported Currencies |


## checkout_create

> <CheckoutResponseDto> checkout_create(create_checkout_dto)

Create Checkout Session

Create a new payment configuration for a product. Returns redirect URLs pointing to the custom checkout layout.

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::CheckoutApi.new
create_checkout_dto = Solifyn::CreateCheckoutDto.new({product_id: 'prod_XXXXXXXXXXX'}) # CreateCheckoutDto | 

begin
  # Create Checkout Session
  result = api_instance.checkout_create(create_checkout_dto)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling CheckoutApi->checkout_create: #{e}"
end
```

#### Using the checkout_create_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CheckoutResponseDto>, Integer, Hash)> checkout_create_with_http_info(create_checkout_dto)

```ruby
begin
  # Create Checkout Session
  data, status_code, headers = api_instance.checkout_create_with_http_info(create_checkout_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CheckoutResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling CheckoutApi->checkout_create_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_checkout_dto** | [**CreateCheckoutDto**](CreateCheckoutDto.md) |  |  |

### Return type

[**CheckoutResponseDto**](CheckoutResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## checkout_create_collection

> <CheckoutResponseDto> checkout_create_collection(create_collection_checkout_dto)

Create Collection Checkout Session

Create a new payment configuration for a product bundle/collection.

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::CheckoutApi.new
create_collection_checkout_dto = Solifyn::CreateCollectionCheckoutDto.new({collection_id: 'col_123'}) # CreateCollectionCheckoutDto | 

begin
  # Create Collection Checkout Session
  result = api_instance.checkout_create_collection(create_collection_checkout_dto)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling CheckoutApi->checkout_create_collection: #{e}"
end
```

#### Using the checkout_create_collection_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CheckoutResponseDto>, Integer, Hash)> checkout_create_collection_with_http_info(create_collection_checkout_dto)

```ruby
begin
  # Create Collection Checkout Session
  data, status_code, headers = api_instance.checkout_create_collection_with_http_info(create_collection_checkout_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CheckoutResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling CheckoutApi->checkout_create_collection_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_collection_checkout_dto** | [**CreateCollectionCheckoutDto**](CreateCollectionCheckoutDto.md) |  |  |

### Return type

[**CheckoutResponseDto**](CheckoutResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## checkout_create_setup

> checkout_create_setup(create_setup_checkout_dto)

Create Setup Checkout Configuration

Create a new checkout session in setup mode for collecting cards without immediate charge.

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::CheckoutApi.new
create_setup_checkout_dto = Solifyn::CreateSetupCheckoutDto.new({company_id: 'biz_xxxxxxxxxxxxxx'}) # CreateSetupCheckoutDto | 

begin
  # Create Setup Checkout Configuration
  api_instance.checkout_create_setup(create_setup_checkout_dto)
rescue Solifyn::ApiError => e
  puts "Error when calling CheckoutApi->checkout_create_setup: #{e}"
end
```

#### Using the checkout_create_setup_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> checkout_create_setup_with_http_info(create_setup_checkout_dto)

```ruby
begin
  # Create Setup Checkout Configuration
  data, status_code, headers = api_instance.checkout_create_setup_with_http_info(create_setup_checkout_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling CheckoutApi->checkout_create_setup_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_setup_checkout_dto** | [**CreateSetupCheckoutDto**](CreateSetupCheckoutDto.md) |  |  |

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## checkout_get_session

> <CheckoutSessionDetailsDto> checkout_get_session(id)

Get Checkout Session Details

Retrieve checkout details to mount the custom embedded checkout.

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::CheckoutApi.new
id = 'ch_XXXXXXXXXXX' # String | Internal database checkout session ID

begin
  # Get Checkout Session Details
  result = api_instance.checkout_get_session(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling CheckoutApi->checkout_get_session: #{e}"
end
```

#### Using the checkout_get_session_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CheckoutSessionDetailsDto>, Integer, Hash)> checkout_get_session_with_http_info(id)

```ruby
begin
  # Get Checkout Session Details
  data, status_code, headers = api_instance.checkout_get_session_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CheckoutSessionDetailsDto>
rescue Solifyn::ApiError => e
  puts "Error when calling CheckoutApi->checkout_get_session_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Internal database checkout session ID |  |

### Return type

[**CheckoutSessionDetailsDto**](CheckoutSessionDetailsDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## checkout_price_preview

> <PricePreviewResponseDto> checkout_price_preview(product_id, addons, opts)

Get Converted Price Preview

Pre-calculate target currencies, applied discounts, and PWYW values before mounting the checkout.

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::CheckoutApi.new
product_id = 'prod_z2o92kEl6cYYX' # String | Public product ID
addons = 'addons_example' # String | 
opts = {
  currency: 'vnd', # String | Target currency code (ISO)
  discount: '10', # String | Percentage discount rate
  qty: '1', # String | Number of product units
  custom_price: '15' # String | Override price for PWYW products
}

begin
  # Get Converted Price Preview
  result = api_instance.checkout_price_preview(product_id, addons, opts)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling CheckoutApi->checkout_price_preview: #{e}"
end
```

#### Using the checkout_price_preview_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PricePreviewResponseDto>, Integer, Hash)> checkout_price_preview_with_http_info(product_id, addons, opts)

```ruby
begin
  # Get Converted Price Preview
  data, status_code, headers = api_instance.checkout_price_preview_with_http_info(product_id, addons, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PricePreviewResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling CheckoutApi->checkout_price_preview_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **String** | Public product ID |  |
| **addons** | **String** |  |  |
| **currency** | **String** | Target currency code (ISO) | [optional] |
| **discount** | **String** | Percentage discount rate | [optional] |
| **qty** | **String** | Number of product units | [optional] |
| **custom_price** | **String** | Override price for PWYW products | [optional] |

### Return type

[**PricePreviewResponseDto**](PricePreviewResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## checkout_supported_currencies

> <Array<SupportedCurrenciesResponseDto>> checkout_supported_currencies

Get Supported Currencies

Retrieve all currencies supported for payouts and conversions.

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::CheckoutApi.new

begin
  # Get Supported Currencies
  result = api_instance.checkout_supported_currencies
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling CheckoutApi->checkout_supported_currencies: #{e}"
end
```

#### Using the checkout_supported_currencies_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<SupportedCurrenciesResponseDto>>, Integer, Hash)> checkout_supported_currencies_with_http_info

```ruby
begin
  # Get Supported Currencies
  data, status_code, headers = api_instance.checkout_supported_currencies_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<SupportedCurrenciesResponseDto>>
rescue Solifyn::ApiError => e
  puts "Error when calling CheckoutApi->checkout_supported_currencies_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;SupportedCurrenciesResponseDto&gt;**](SupportedCurrenciesResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

