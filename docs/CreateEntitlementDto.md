# Solifyn::CreateEntitlementDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | The user-friendly name of the entitlement |  |
| **type** | **String** | The type of access to grant |  |
| **github_repo** | **String** | The GitHub repository (e.g., owner/repo) | [optional] |
| **github_permission** | **String** | The GitHub repository permission level | [optional][default to &#39;pull&#39;] |
| **discord_guild_id** | **String** | The Discord Guild/Server ID | [optional] |
| **discord_role_id** | **String** | The Discord Role ID to assign | [optional] |
| **framer_template_id** | **String** | The associated Framer Template ID | [optional] |
| **license_key** | **String** | The static License Key (if not dynamically generated) | [optional] |
| **activation_limit** | **Float** | The maximum activation limit for licenses | [optional] |
| **activation_message** | **String** | A message shown to the user upon license activation | [optional] |
| **expiry_hours** | **Float** | The number of hours until the entitlement expires | [optional] |
| **digital_link** | **String** | The digital download URL or redirect link | [optional] |
| **instructions** | **String** | Custom setup instructions for the user | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::CreateEntitlementDto.new(
  name: Premium GitHub Access,
  type: GITHUB,
  github_repo: solifyn/premium-repo,
  github_permission: pull,
  discord_guild_id: 123456789012345678,
  discord_role_id: 876543210987654321,
  framer_template_id: framer_tmpl_123,
  license_key: whsec_license_key_123,
  activation_limit: 3,
  activation_message: Thank you for activating your software license!,
  expiry_hours: 720,
  digital_link: https://downloads.solifyn.com/file.zip,
  instructions: Clone the repository and run npm install.
)
```

