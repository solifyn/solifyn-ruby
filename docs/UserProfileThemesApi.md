# Solifyn::UserProfileThemesApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**users_get_my_page**](UserProfileThemesApi.md#users_get_my_page) | **GET** /v1/user/my-page | Get My Page details |
| [**users_get_my_theme**](UserProfileThemesApi.md#users_get_my_theme) | **GET** /v1/user/my-theme | Get My Theme |
| [**users_get_settings**](UserProfileThemesApi.md#users_get_settings) | **GET** /v1/user/settings | Retrieve User Settings |
| [**users_get_stats**](UserProfileThemesApi.md#users_get_stats) | **GET** /v1/user/dashboard-stats | Get Dashboard Statistics |
| [**users_get_theme_by_subdomain**](UserProfileThemesApi.md#users_get_theme_by_subdomain) | **GET** /v1/user/theme/{subdomain} | Get Theme by Subdomain |


## users_get_my_page

> <UserPage> users_get_my_page

Get My Page details

Retrieve page settings and custom content configured for the store.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::UserProfileThemesApi.new

begin
  # Get My Page details
  result = api_instance.users_get_my_page
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling UserProfileThemesApi->users_get_my_page: #{e}"
end
```

#### Using the users_get_my_page_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UserPage>, Integer, Hash)> users_get_my_page_with_http_info

```ruby
begin
  # Get My Page details
  data, status_code, headers = api_instance.users_get_my_page_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UserPage>
rescue Solifyn::ApiError => e
  puts "Error when calling UserProfileThemesApi->users_get_my_page_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**UserPage**](UserPage.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## users_get_my_theme

> <UserTheme> users_get_my_theme

Get My Theme

Retrieve theme configurations for the active business context.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::UserProfileThemesApi.new

begin
  # Get My Theme
  result = api_instance.users_get_my_theme
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling UserProfileThemesApi->users_get_my_theme: #{e}"
end
```

#### Using the users_get_my_theme_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UserTheme>, Integer, Hash)> users_get_my_theme_with_http_info

```ruby
begin
  # Get My Theme
  data, status_code, headers = api_instance.users_get_my_theme_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UserTheme>
rescue Solifyn::ApiError => e
  puts "Error when calling UserProfileThemesApi->users_get_my_theme_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**UserTheme**](UserTheme.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## users_get_settings

> <UserSettings> users_get_settings

Retrieve User Settings

Retrieve profile settings and notification preferences for the user.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::UserProfileThemesApi.new

begin
  # Retrieve User Settings
  result = api_instance.users_get_settings
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling UserProfileThemesApi->users_get_settings: #{e}"
end
```

#### Using the users_get_settings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UserSettings>, Integer, Hash)> users_get_settings_with_http_info

```ruby
begin
  # Retrieve User Settings
  data, status_code, headers = api_instance.users_get_settings_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UserSettings>
rescue Solifyn::ApiError => e
  puts "Error when calling UserProfileThemesApi->users_get_settings_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**UserSettings**](UserSettings.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## users_get_stats

> <UserStats> users_get_stats

Get Dashboard Statistics

Retrieve general analytics stats (revenue, order counts, etc.) for dashboard graphs.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::UserProfileThemesApi.new

begin
  # Get Dashboard Statistics
  result = api_instance.users_get_stats
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling UserProfileThemesApi->users_get_stats: #{e}"
end
```

#### Using the users_get_stats_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UserStats>, Integer, Hash)> users_get_stats_with_http_info

```ruby
begin
  # Get Dashboard Statistics
  data, status_code, headers = api_instance.users_get_stats_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UserStats>
rescue Solifyn::ApiError => e
  puts "Error when calling UserProfileThemesApi->users_get_stats_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**UserStats**](UserStats.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## users_get_theme_by_subdomain

> <UserTheme> users_get_theme_by_subdomain(subdomain)

Get Theme by Subdomain

Retrieve public theme configuration details by store subdomain.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::UserProfileThemesApi.new
subdomain = 'acme' # String | The subdomain of the store

begin
  # Get Theme by Subdomain
  result = api_instance.users_get_theme_by_subdomain(subdomain)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling UserProfileThemesApi->users_get_theme_by_subdomain: #{e}"
end
```

#### Using the users_get_theme_by_subdomain_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UserTheme>, Integer, Hash)> users_get_theme_by_subdomain_with_http_info(subdomain)

```ruby
begin
  # Get Theme by Subdomain
  data, status_code, headers = api_instance.users_get_theme_by_subdomain_with_http_info(subdomain)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UserTheme>
rescue Solifyn::ApiError => e
  puts "Error when calling UserProfileThemesApi->users_get_theme_by_subdomain_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **subdomain** | **String** | The subdomain of the store |  |

### Return type

[**UserTheme**](UserTheme.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

