# Solifyn::DiscordIntegrationApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**discord_get_install_url**](DiscordIntegrationApi.md#discord_get_install_url) | **GET** /v1/discord/install | Get Discord Bot Installation URL |
| [**discord_list_roles**](DiscordIntegrationApi.md#discord_list_roles) | **GET** /v1/discord/roles | List Guild Discord Roles |


## discord_get_install_url

> discord_get_install_url(opts)

Get Discord Bot Installation URL

Generates the URL to invite the system-wide Discord Bot onto the merchant's Discord server.

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::DiscordIntegrationApi.new
opts = {
  product_id: 'product_id_example' # String | Optional Product ID to redirect back to after installation
}

begin
  # Get Discord Bot Installation URL
  api_instance.discord_get_install_url(opts)
rescue Solifyn::ApiError => e
  puts "Error when calling DiscordIntegrationApi->discord_get_install_url: #{e}"
end
```

#### Using the discord_get_install_url_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> discord_get_install_url_with_http_info(opts)

```ruby
begin
  # Get Discord Bot Installation URL
  data, status_code, headers = api_instance.discord_get_install_url_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DiscordIntegrationApi->discord_get_install_url_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **String** | Optional Product ID to redirect back to after installation | [optional] |

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## discord_list_roles

> <Array<DiscordRolesResponseDto>> discord_list_roles

List Guild Discord Roles

Retrieves all roles available in the connected merchant's Discord server/guild.

### Examples

```ruby
require 'time'
require 'solifyn'

api_instance = Solifyn::DiscordIntegrationApi.new

begin
  # List Guild Discord Roles
  result = api_instance.discord_list_roles
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling DiscordIntegrationApi->discord_list_roles: #{e}"
end
```

#### Using the discord_list_roles_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<DiscordRolesResponseDto>>, Integer, Hash)> discord_list_roles_with_http_info

```ruby
begin
  # List Guild Discord Roles
  data, status_code, headers = api_instance.discord_list_roles_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<DiscordRolesResponseDto>>
rescue Solifyn::ApiError => e
  puts "Error when calling DiscordIntegrationApi->discord_list_roles_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;DiscordRolesResponseDto&gt;**](DiscordRolesResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

