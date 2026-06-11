# Solifyn::FramerIntegrationApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**framer_create_template**](FramerIntegrationApi.md#framer_create_template) | **POST** /v1/framer/templates | Create Framer Template |
| [**framer_delete_template**](FramerIntegrationApi.md#framer_delete_template) | **DELETE** /v1/framer/templates/{id} | Delete Framer Template |
| [**framer_get_template**](FramerIntegrationApi.md#framer_get_template) | **GET** /v1/framer/templates/{id} | Retrieve Framer Template |
| [**framer_list_templates**](FramerIntegrationApi.md#framer_list_templates) | **GET** /v1/framer/templates | List Framer Templates |
| [**framer_update_template**](FramerIntegrationApi.md#framer_update_template) | **PUT** /v1/framer/templates/{id} | Update Framer Template |


## framer_create_template

> <FramerTemplateResponseDto> framer_create_template(create_framer_template_dto)

Create Framer Template

Registers a new Framer template with its public remix link for the active business.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::FramerIntegrationApi.new
create_framer_template_dto = Solifyn::CreateFramerTemplateDto.new({name: 'Portfolio Template', remix_link: 'https://framer.com/projects/xyz'}) # CreateFramerTemplateDto | 

begin
  # Create Framer Template
  result = api_instance.framer_create_template(create_framer_template_dto)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling FramerIntegrationApi->framer_create_template: #{e}"
end
```

#### Using the framer_create_template_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FramerTemplateResponseDto>, Integer, Hash)> framer_create_template_with_http_info(create_framer_template_dto)

```ruby
begin
  # Create Framer Template
  data, status_code, headers = api_instance.framer_create_template_with_http_info(create_framer_template_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FramerTemplateResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling FramerIntegrationApi->framer_create_template_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_framer_template_dto** | [**CreateFramerTemplateDto**](CreateFramerTemplateDto.md) |  |  |

### Return type

[**FramerTemplateResponseDto**](FramerTemplateResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## framer_delete_template

> framer_delete_template(id)

Delete Framer Template

Deletes a registered Framer template for the active business.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::FramerIntegrationApi.new
id = 'id_example' # String | The Framer template ID

begin
  # Delete Framer Template
  api_instance.framer_delete_template(id)
rescue Solifyn::ApiError => e
  puts "Error when calling FramerIntegrationApi->framer_delete_template: #{e}"
end
```

#### Using the framer_delete_template_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> framer_delete_template_with_http_info(id)

```ruby
begin
  # Delete Framer Template
  data, status_code, headers = api_instance.framer_delete_template_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling FramerIntegrationApi->framer_delete_template_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The Framer template ID |  |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## framer_get_template

> <FramerTemplateResponseDto> framer_get_template(id)

Retrieve Framer Template

Retrieves details of a specific registered Framer template.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::FramerIntegrationApi.new
id = 'id_example' # String | The Framer template ID

begin
  # Retrieve Framer Template
  result = api_instance.framer_get_template(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling FramerIntegrationApi->framer_get_template: #{e}"
end
```

#### Using the framer_get_template_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FramerTemplateResponseDto>, Integer, Hash)> framer_get_template_with_http_info(id)

```ruby
begin
  # Retrieve Framer Template
  data, status_code, headers = api_instance.framer_get_template_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FramerTemplateResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling FramerIntegrationApi->framer_get_template_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The Framer template ID |  |

### Return type

[**FramerTemplateResponseDto**](FramerTemplateResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## framer_list_templates

> <Array<FramerTemplateResponseDto>> framer_list_templates

List Framer Templates

Retrieves all registered Framer templates for the active business.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::FramerIntegrationApi.new

begin
  # List Framer Templates
  result = api_instance.framer_list_templates
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling FramerIntegrationApi->framer_list_templates: #{e}"
end
```

#### Using the framer_list_templates_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<FramerTemplateResponseDto>>, Integer, Hash)> framer_list_templates_with_http_info

```ruby
begin
  # List Framer Templates
  data, status_code, headers = api_instance.framer_list_templates_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<FramerTemplateResponseDto>>
rescue Solifyn::ApiError => e
  puts "Error when calling FramerIntegrationApi->framer_list_templates_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;FramerTemplateResponseDto&gt;**](FramerTemplateResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## framer_update_template

> <FramerTemplateResponseDto> framer_update_template(id, update_framer_template_dto)

Update Framer Template

Updates a registered Framer template for the active business.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::FramerIntegrationApi.new
id = 'id_example' # String | The Framer template ID
update_framer_template_dto = Solifyn::UpdateFramerTemplateDto.new # UpdateFramerTemplateDto | 

begin
  # Update Framer Template
  result = api_instance.framer_update_template(id, update_framer_template_dto)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling FramerIntegrationApi->framer_update_template: #{e}"
end
```

#### Using the framer_update_template_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FramerTemplateResponseDto>, Integer, Hash)> framer_update_template_with_http_info(id, update_framer_template_dto)

```ruby
begin
  # Update Framer Template
  data, status_code, headers = api_instance.framer_update_template_with_http_info(id, update_framer_template_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FramerTemplateResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling FramerIntegrationApi->framer_update_template_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The Framer template ID |  |
| **update_framer_template_dto** | [**UpdateFramerTemplateDto**](UpdateFramerTemplateDto.md) |  |  |

### Return type

[**FramerTemplateResponseDto**](FramerTemplateResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

