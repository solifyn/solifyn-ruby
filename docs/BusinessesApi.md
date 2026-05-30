# Solifyn::BusinessesApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**businesses_billing_history**](BusinessesApi.md#businesses_billing_history) | **GET** /v1/user/billing/history | Get Platform Billing History |
| [**merchants_generate_api_keys**](BusinessesApi.md#merchants_generate_api_keys) | **POST** /v1/user/whop-api-keys | Rotate Whop API Keys |
| [**merchants_update_page**](BusinessesApi.md#merchants_update_page) | **PATCH** /v1/user/page | Update Page configuration |
| [**merchants_update_settings**](BusinessesApi.md#merchants_update_settings) | **PATCH** /v1/user/settings | Update Merchant Settings |
| [**merchants_update_theme**](BusinessesApi.md#merchants_update_theme) | **PATCH** /v1/user/theme | Update Theme |


## businesses_billing_history

> businesses_billing_history

Get Platform Billing History

Retrieve history of SaaS subscription payments paid by this business to the platform.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::BusinessesApi.new

begin
  # Get Platform Billing History
  api_instance.businesses_billing_history
rescue Solifyn::ApiError => e
  puts "Error when calling BusinessesApi->businesses_billing_history: #{e}"
end
```

#### Using the businesses_billing_history_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> businesses_billing_history_with_http_info

```ruby
begin
  # Get Platform Billing History
  data, status_code, headers = api_instance.businesses_billing_history_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling BusinessesApi->businesses_billing_history_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## merchants_generate_api_keys

> <WhopApiKeysRotation> merchants_generate_api_keys

Rotate Whop API Keys

Generate and sync a new Whop Child Company API key (restricted to business owners).

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::BusinessesApi.new

begin
  # Rotate Whop API Keys
  result = api_instance.merchants_generate_api_keys
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling BusinessesApi->merchants_generate_api_keys: #{e}"
end
```

#### Using the merchants_generate_api_keys_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WhopApiKeysRotation>, Integer, Hash)> merchants_generate_api_keys_with_http_info

```ruby
begin
  # Rotate Whop API Keys
  data, status_code, headers = api_instance.merchants_generate_api_keys_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WhopApiKeysRotation>
rescue Solifyn::ApiError => e
  puts "Error when calling BusinessesApi->merchants_generate_api_keys_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**WhopApiKeysRotation**](WhopApiKeysRotation.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## merchants_update_page

> <UserPage> merchants_update_page(user_theme_update)

Update Page configuration

Modify store page content configs, banner images, or avatar details.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::BusinessesApi.new
user_theme_update = Solifyn::UserThemeUpdate.new # UserThemeUpdate | 

begin
  # Update Page configuration
  result = api_instance.merchants_update_page(user_theme_update)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling BusinessesApi->merchants_update_page: #{e}"
end
```

#### Using the merchants_update_page_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UserPage>, Integer, Hash)> merchants_update_page_with_http_info(user_theme_update)

```ruby
begin
  # Update Page configuration
  data, status_code, headers = api_instance.merchants_update_page_with_http_info(user_theme_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UserPage>
rescue Solifyn::ApiError => e
  puts "Error when calling BusinessesApi->merchants_update_page_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **user_theme_update** | [**UserThemeUpdate**](UserThemeUpdate.md) |  |  |

### Return type

[**UserPage**](UserPage.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## merchants_update_settings

> <UserSettings> merchants_update_settings(user_settings_update)

Update Merchant Settings

Update profile parameters, SEO, Google analytics, and email notification properties.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::BusinessesApi.new
user_settings_update = Solifyn::UserSettingsUpdate.new # UserSettingsUpdate | 

begin
  # Update Merchant Settings
  result = api_instance.merchants_update_settings(user_settings_update)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling BusinessesApi->merchants_update_settings: #{e}"
end
```

#### Using the merchants_update_settings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UserSettings>, Integer, Hash)> merchants_update_settings_with_http_info(user_settings_update)

```ruby
begin
  # Update Merchant Settings
  data, status_code, headers = api_instance.merchants_update_settings_with_http_info(user_settings_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UserSettings>
rescue Solifyn::ApiError => e
  puts "Error when calling BusinessesApi->merchants_update_settings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **user_settings_update** | [**UserSettingsUpdate**](UserSettingsUpdate.md) |  |  |

### Return type

[**UserSettings**](UserSettings.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## merchants_update_theme

> <UserTheme> merchants_update_theme(user_theme_update)

Update Theme

Update colors, fonts, avatar, or banner settings for the store.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::BusinessesApi.new
user_theme_update = Solifyn::UserThemeUpdate.new # UserThemeUpdate | 

begin
  # Update Theme
  result = api_instance.merchants_update_theme(user_theme_update)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling BusinessesApi->merchants_update_theme: #{e}"
end
```

#### Using the merchants_update_theme_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UserTheme>, Integer, Hash)> merchants_update_theme_with_http_info(user_theme_update)

```ruby
begin
  # Update Theme
  data, status_code, headers = api_instance.merchants_update_theme_with_http_info(user_theme_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UserTheme>
rescue Solifyn::ApiError => e
  puts "Error when calling BusinessesApi->merchants_update_theme_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **user_theme_update** | [**UserThemeUpdate**](UserThemeUpdate.md) |  |  |

### Return type

[**UserTheme**](UserTheme.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

