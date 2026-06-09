# Solifyn::LicenseKeysClientApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**licenses_activate**](LicenseKeysClientApi.md#licenses_activate) | **POST** /v1/licenses/activate | Activate License Key |
| [**licenses_deactivate**](LicenseKeysClientApi.md#licenses_deactivate) | **POST** /v1/licenses/deactivate/{instanceId} | Deactivate Instance |
| [**licenses_instances**](LicenseKeysClientApi.md#licenses_instances) | **GET** /v1/licenses/instances/{licenseId} | Get Active Instances |
| [**licenses_verify**](LicenseKeysClientApi.md#licenses_verify) | **POST** /v1/licenses/verify | Validate License Key |


## licenses_activate

> <Instance> licenses_activate(licenses_activate_request)

Activate License Key

Register and activate a device or instance for a specific license key.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::LicenseKeysClientApi.new
licenses_activate_request = Solifyn::LicensesActivateRequest.new({key: 'key_example', device_identifier: 'device_identifier_example', name: 'name_example'}) # LicensesActivateRequest | 

begin
  # Activate License Key
  result = api_instance.licenses_activate(licenses_activate_request)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling LicenseKeysClientApi->licenses_activate: #{e}"
end
```

#### Using the licenses_activate_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Instance>, Integer, Hash)> licenses_activate_with_http_info(licenses_activate_request)

```ruby
begin
  # Activate License Key
  data, status_code, headers = api_instance.licenses_activate_with_http_info(licenses_activate_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Instance>
rescue Solifyn::ApiError => e
  puts "Error when calling LicenseKeysClientApi->licenses_activate_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **licenses_activate_request** | [**LicensesActivateRequest**](LicensesActivateRequest.md) |  |  |

### Return type

[**Instance**](Instance.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## licenses_deactivate

> <LicensesDeactivate200Response> licenses_deactivate(instance_id, licenses_deactivate_request)

Deactivate Instance

Deactivate or unregister an active device instance from a license key.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::LicenseKeysClientApi.new
instance_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | The unique device instance ID.
licenses_deactivate_request = Solifyn::LicensesDeactivateRequest.new({key: 'key_example'}) # LicensesDeactivateRequest | 

begin
  # Deactivate Instance
  result = api_instance.licenses_deactivate(instance_id, licenses_deactivate_request)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling LicenseKeysClientApi->licenses_deactivate: #{e}"
end
```

#### Using the licenses_deactivate_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<LicensesDeactivate200Response>, Integer, Hash)> licenses_deactivate_with_http_info(instance_id, licenses_deactivate_request)

```ruby
begin
  # Deactivate Instance
  data, status_code, headers = api_instance.licenses_deactivate_with_http_info(instance_id, licenses_deactivate_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <LicensesDeactivate200Response>
rescue Solifyn::ApiError => e
  puts "Error when calling LicenseKeysClientApi->licenses_deactivate_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **instance_id** | **String** | The unique device instance ID. |  |
| **licenses_deactivate_request** | [**LicensesDeactivateRequest**](LicensesDeactivateRequest.md) |  |  |

### Return type

[**LicensesDeactivate200Response**](LicensesDeactivate200Response.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## licenses_instances

> <Array<Instance>> licenses_instances(license_id)

Get Active Instances

List all active devices or server instances linked to a specific license key.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::LicenseKeysClientApi.new
license_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | The unique license key ID.

begin
  # Get Active Instances
  result = api_instance.licenses_instances(license_id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling LicenseKeysClientApi->licenses_instances: #{e}"
end
```

#### Using the licenses_instances_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Instance>>, Integer, Hash)> licenses_instances_with_http_info(license_id)

```ruby
begin
  # Get Active Instances
  data, status_code, headers = api_instance.licenses_instances_with_http_info(license_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Instance>>
rescue Solifyn::ApiError => e
  puts "Error when calling LicenseKeysClientApi->licenses_instances_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **license_id** | **String** | The unique license key ID. |  |

### Return type

[**Array&lt;Instance&gt;**](Instance.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## licenses_verify

> <LicenseValidationResponse> licenses_verify(licenses_verify_request)

Validate License Key

Verify if a software license key is valid, active, and has not exceeded its limits.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::LicenseKeysClientApi.new
licenses_verify_request = Solifyn::LicensesVerifyRequest.new({key: 'key_example', product_id: 'product_id_example'}) # LicensesVerifyRequest | 

begin
  # Validate License Key
  result = api_instance.licenses_verify(licenses_verify_request)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling LicenseKeysClientApi->licenses_verify: #{e}"
end
```

#### Using the licenses_verify_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<LicenseValidationResponse>, Integer, Hash)> licenses_verify_with_http_info(licenses_verify_request)

```ruby
begin
  # Validate License Key
  data, status_code, headers = api_instance.licenses_verify_with_http_info(licenses_verify_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <LicenseValidationResponse>
rescue Solifyn::ApiError => e
  puts "Error when calling LicenseKeysClientApi->licenses_verify_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **licenses_verify_request** | [**LicensesVerifyRequest**](LicensesVerifyRequest.md) |  |  |

### Return type

[**LicenseValidationResponse**](LicenseValidationResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

