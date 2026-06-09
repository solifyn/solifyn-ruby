# Solifyn::GithubReposResponseDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Float** | The GitHub repository ID |  |
| **full_name** | **String** | The repository full name (owner/repo) |  |
| **name** | **String** | The repository name |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::GithubReposResponseDto.new(
  id: 12345678,
  full_name: solifyn/premium-app,
  name: premium-app
)
```

