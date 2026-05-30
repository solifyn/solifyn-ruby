# Solifyn::LicenseApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**licenses_create**](LicenseApi.md#licenses_create) | **POST** /v1/licenses | Create License Key |
| [**licenses_delete_instance**](LicenseApi.md#licenses_delete_instance) | **DELETE** /v1/licenses/instances/{instanceId} | Force Delete Instance |
| [**licenses_get**](LicenseApi.md#licenses_get) | **GET** /v1/licenses/{id} | Get License Key |
| [**licenses_get_instance**](LicenseApi.md#licenses_get_instance) | **GET** /v1/licenses/{id}/instances/{instanceId} | Get License Key Instance |
| [**licenses_get_instances**](LicenseApi.md#licenses_get_instances) | **GET** /v1/licenses/{id}/instances | Get License Key Instances |
| [**licenses_list**](LicenseApi.md#licenses_list) | **GET** /v1/licenses | List License Keys |
| [**licenses_toggle**](LicenseApi.md#licenses_toggle) | **POST** /v1/licenses/{id}/toggle | Toggle License Status |
| [**licenses_update**](LicenseApi.md#licenses_update) | **PATCH** /v1/licenses/{id} | Update License Key |
| [**licenses_update_instance**](LicenseApi.md#licenses_update_instance) | **PATCH** /v1/licenses/{id}/instances/{instanceId} | Update License Key Instance |
| [**licenses_update_instance_post**](LicenseApi.md#licenses_update_instance_post) | **POST** /v1/licenses/{id}/instances/{instanceId} | Update License Key Instance (POST) |


## licenses_create

> <License> licenses_create(licenses_create_request)

Create License Key

Manually issue a new license key for a specific product.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::LicenseApi.new
licenses_create_request = Solifyn::LicensesCreateRequest.new({product_id: 'product_id_example', customer_id: 'customer_id_example'}) # LicensesCreateRequest | 

begin
  # Create License Key
  result = api_instance.licenses_create(licenses_create_request)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling LicenseApi->licenses_create: #{e}"
end
```

#### Using the licenses_create_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<License>, Integer, Hash)> licenses_create_with_http_info(licenses_create_request)

```ruby
begin
  # Create License Key
  data, status_code, headers = api_instance.licenses_create_with_http_info(licenses_create_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <License>
rescue Solifyn::ApiError => e
  puts "Error when calling LicenseApi->licenses_create_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **licenses_create_request** | [**LicensesCreateRequest**](LicensesCreateRequest.md) |  |  |

### Return type

[**License**](License.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## licenses_delete_instance

> <Instance> licenses_delete_instance(instance_id)

Force Delete Instance

Administrative endpoint to force-delete an instance globally by its database ID.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::LicenseApi.new
instance_id = 'inc_123' # String | The unique hardware activation instance ID.

begin
  # Force Delete Instance
  result = api_instance.licenses_delete_instance(instance_id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling LicenseApi->licenses_delete_instance: #{e}"
end
```

#### Using the licenses_delete_instance_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Instance>, Integer, Hash)> licenses_delete_instance_with_http_info(instance_id)

```ruby
begin
  # Force Delete Instance
  data, status_code, headers = api_instance.licenses_delete_instance_with_http_info(instance_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Instance>
rescue Solifyn::ApiError => e
  puts "Error when calling LicenseApi->licenses_delete_instance_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **instance_id** | **String** | The unique hardware activation instance ID. |  |

### Return type

[**Instance**](Instance.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## licenses_get

> <License> licenses_get(id)

Get License Key

Retrieve complete administrative details of a specific license key.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::LicenseApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | The unique license key ID.

begin
  # Get License Key
  result = api_instance.licenses_get(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling LicenseApi->licenses_get: #{e}"
end
```

#### Using the licenses_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<License>, Integer, Hash)> licenses_get_with_http_info(id)

```ruby
begin
  # Get License Key
  data, status_code, headers = api_instance.licenses_get_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <License>
rescue Solifyn::ApiError => e
  puts "Error when calling LicenseApi->licenses_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique license key ID. |  |

### Return type

[**License**](License.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## licenses_get_instance

> <Instance> licenses_get_instance(id, instance_id)

Get License Key Instance

Retrieve administrative details of a specific software license instance.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::LicenseApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | The unique administrative identifier (ID) of the parent license key.
instance_id = 'inc_123' # String | The client-generated instance ID (hardware hash) or the internal database ID of the instance.

begin
  # Get License Key Instance
  result = api_instance.licenses_get_instance(id, instance_id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling LicenseApi->licenses_get_instance: #{e}"
end
```

#### Using the licenses_get_instance_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Instance>, Integer, Hash)> licenses_get_instance_with_http_info(id, instance_id)

```ruby
begin
  # Get License Key Instance
  data, status_code, headers = api_instance.licenses_get_instance_with_http_info(id, instance_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Instance>
rescue Solifyn::ApiError => e
  puts "Error when calling LicenseApi->licenses_get_instance_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique administrative identifier (ID) of the parent license key. |  |
| **instance_id** | **String** | The client-generated instance ID (hardware hash) or the internal database ID of the instance. |  |

### Return type

[**Instance**](Instance.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## licenses_get_instances

> <Array<Instance>> licenses_get_instances(id)

Get License Key Instances

Retrieve all active devices/instances for a specific administrative license key.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::LicenseApi.new
id = 'lic_123' # String | The unique administrative identifier (ID) of the parent license key.

begin
  # Get License Key Instances
  result = api_instance.licenses_get_instances(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling LicenseApi->licenses_get_instances: #{e}"
end
```

#### Using the licenses_get_instances_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Instance>>, Integer, Hash)> licenses_get_instances_with_http_info(id)

```ruby
begin
  # Get License Key Instances
  data, status_code, headers = api_instance.licenses_get_instances_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Instance>>
rescue Solifyn::ApiError => e
  puts "Error when calling LicenseApi->licenses_get_instances_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique administrative identifier (ID) of the parent license key. |  |

### Return type

[**Array&lt;Instance&gt;**](Instance.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## licenses_list

> <Array<License>> licenses_list

List License Keys

List all administrative license keys belonging to products under your active business.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::LicenseApi.new

begin
  # List License Keys
  result = api_instance.licenses_list
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling LicenseApi->licenses_list: #{e}"
end
```

#### Using the licenses_list_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<License>>, Integer, Hash)> licenses_list_with_http_info

```ruby
begin
  # List License Keys
  data, status_code, headers = api_instance.licenses_list_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<License>>
rescue Solifyn::ApiError => e
  puts "Error when calling LicenseApi->licenses_list_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;License&gt;**](License.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## licenses_toggle

> <License> licenses_toggle(id)

Toggle License Status

Toggle the status of a specific license key between ACTIVE and DISABLED.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::LicenseApi.new
id = 'lic_123' # String | The unique license key ID.

begin
  # Toggle License Status
  result = api_instance.licenses_toggle(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling LicenseApi->licenses_toggle: #{e}"
end
```

#### Using the licenses_toggle_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<License>, Integer, Hash)> licenses_toggle_with_http_info(id)

```ruby
begin
  # Toggle License Status
  data, status_code, headers = api_instance.licenses_toggle_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <License>
rescue Solifyn::ApiError => e
  puts "Error when calling LicenseApi->licenses_toggle_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique license key ID. |  |

### Return type

[**License**](License.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## licenses_update

> <License> licenses_update(id, licenses_update_request)

Update License Key

Update limits or status of an existing license key.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::LicenseApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | The unique license key ID.
licenses_update_request = Solifyn::LicensesUpdateRequest.new # LicensesUpdateRequest | 

begin
  # Update License Key
  result = api_instance.licenses_update(id, licenses_update_request)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling LicenseApi->licenses_update: #{e}"
end
```

#### Using the licenses_update_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<License>, Integer, Hash)> licenses_update_with_http_info(id, licenses_update_request)

```ruby
begin
  # Update License Key
  data, status_code, headers = api_instance.licenses_update_with_http_info(id, licenses_update_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <License>
rescue Solifyn::ApiError => e
  puts "Error when calling LicenseApi->licenses_update_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique license key ID. |  |
| **licenses_update_request** | [**LicensesUpdateRequest**](LicensesUpdateRequest.md) |  |  |

### Return type

[**License**](License.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## licenses_update_instance

> <Instance> licenses_update_instance(instance_id, id, licenses_update_instance_post_request)

Update License Key Instance

Update administrative details (like friendly display name or custom IP) of an active license device instance.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::LicenseApi.new
instance_id = 'inc_123' # String | The client-generated instance ID (hardware hash) or the internal database ID of the instance.
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | The unique administrative identifier (ID) of the parent license key.
licenses_update_instance_post_request = Solifyn::LicensesUpdateInstancePostRequest.new # LicensesUpdateInstancePostRequest | 

begin
  # Update License Key Instance
  result = api_instance.licenses_update_instance(instance_id, id, licenses_update_instance_post_request)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling LicenseApi->licenses_update_instance: #{e}"
end
```

#### Using the licenses_update_instance_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Instance>, Integer, Hash)> licenses_update_instance_with_http_info(instance_id, id, licenses_update_instance_post_request)

```ruby
begin
  # Update License Key Instance
  data, status_code, headers = api_instance.licenses_update_instance_with_http_info(instance_id, id, licenses_update_instance_post_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Instance>
rescue Solifyn::ApiError => e
  puts "Error when calling LicenseApi->licenses_update_instance_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **instance_id** | **String** | The client-generated instance ID (hardware hash) or the internal database ID of the instance. |  |
| **id** | **String** | The unique administrative identifier (ID) of the parent license key. |  |
| **licenses_update_instance_post_request** | [**LicensesUpdateInstancePostRequest**](LicensesUpdateInstancePostRequest.md) |  |  |

### Return type

[**Instance**](Instance.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## licenses_update_instance_post

> <Instance> licenses_update_instance_post(instance_id, id, licenses_update_instance_post_request)

Update License Key Instance (POST)

Alternative POST endpoint to update administrative details (like friendly display name or custom IP) of an active license device instance.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::LicenseApi.new
instance_id = 'inc_123' # String | The client-generated instance ID (hardware hash) or the internal database ID of the instance.
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | The unique administrative identifier (ID) of the parent license key.
licenses_update_instance_post_request = Solifyn::LicensesUpdateInstancePostRequest.new # LicensesUpdateInstancePostRequest | 

begin
  # Update License Key Instance (POST)
  result = api_instance.licenses_update_instance_post(instance_id, id, licenses_update_instance_post_request)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling LicenseApi->licenses_update_instance_post: #{e}"
end
```

#### Using the licenses_update_instance_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Instance>, Integer, Hash)> licenses_update_instance_post_with_http_info(instance_id, id, licenses_update_instance_post_request)

```ruby
begin
  # Update License Key Instance (POST)
  data, status_code, headers = api_instance.licenses_update_instance_post_with_http_info(instance_id, id, licenses_update_instance_post_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Instance>
rescue Solifyn::ApiError => e
  puts "Error when calling LicenseApi->licenses_update_instance_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **instance_id** | **String** | The client-generated instance ID (hardware hash) or the internal database ID of the instance. |  |
| **id** | **String** | The unique administrative identifier (ID) of the parent license key. |  |
| **licenses_update_instance_post_request** | [**LicensesUpdateInstancePostRequest**](LicensesUpdateInstancePostRequest.md) |  |  |

### Return type

[**Instance**](Instance.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

