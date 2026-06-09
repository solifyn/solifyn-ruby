# Solifyn::GitHubIntegrationApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**github_get_install_url**](GitHubIntegrationApi.md#github_get_install_url) | **GET** /v1/github/install | Get GitHub App Installation URL |
| [**github_list_repos**](GitHubIntegrationApi.md#github_list_repos) | **GET** /v1/github/repos | List Available GitHub Repositories |


## github_get_install_url

> github_get_install_url(opts)

Get GitHub App Installation URL

Generates the URL to install the system-wide GitHub App onto the merchant's GitHub account/org.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::GitHubIntegrationApi.new
opts = {
  product_id: 'product_id_example' # String | Optional Product ID to redirect back to after installation
}

begin
  # Get GitHub App Installation URL
  api_instance.github_get_install_url(opts)
rescue Solifyn::ApiError => e
  puts "Error when calling GitHubIntegrationApi->github_get_install_url: #{e}"
end
```

#### Using the github_get_install_url_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> github_get_install_url_with_http_info(opts)

```ruby
begin
  # Get GitHub App Installation URL
  data, status_code, headers = api_instance.github_get_install_url_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling GitHubIntegrationApi->github_get_install_url_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **String** | Optional Product ID to redirect back to after installation | [optional] |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## github_list_repos

> <Array<GithubReposResponseDto>> github_list_repos

List Available GitHub Repositories

Retrieves all repositories accessible by the merchant's installed GitHub App.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::GitHubIntegrationApi.new

begin
  # List Available GitHub Repositories
  result = api_instance.github_list_repos
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling GitHubIntegrationApi->github_list_repos: #{e}"
end
```

#### Using the github_list_repos_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<GithubReposResponseDto>>, Integer, Hash)> github_list_repos_with_http_info

```ruby
begin
  # List Available GitHub Repositories
  data, status_code, headers = api_instance.github_list_repos_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<GithubReposResponseDto>>
rescue Solifyn::ApiError => e
  puts "Error when calling GitHubIntegrationApi->github_list_repos_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;GithubReposResponseDto&gt;**](GithubReposResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

