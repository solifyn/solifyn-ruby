# Solifyn::EntitlementDetailResponseDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique entitlement ID |  |
| **business_id** | **String** | The owning business ID |  |
| **name** | **String** | The name of the entitlement |  |
| **type** | **String** | The type of access to grant |  |
| **status** | **String** | Status of the entitlement |  |
| **created_at** | **Time** | When the entitlement was created |  |
| **updated_at** | **Time** | When the entitlement was last updated |  |
| **github_repo** | **String** | The GitHub repository (e.g., owner/repo) | [optional] |
| **github_permission** | **String** | The GitHub repository permission level | [optional] |
| **discord_guild_id** | **String** | The Discord Guild/Server ID | [optional] |
| **discord_role_id** | **String** | The Discord Role ID to assign | [optional] |
| **framer_template_id** | **String** | The associated Framer Template ID | [optional] |
| **license_key** | **String** | The static License Key (if not dynamically generated) | [optional] |
| **activation_limit** | **Float** | The maximum activation limit for licenses | [optional] |
| **activation_message** | **String** | A message shown to the user upon license activation | [optional] |
| **expiry_hours** | **Float** | The number of hours until the entitlement expires | [optional] |
| **digital_link** | **String** | The digital download URL or redirect link | [optional] |
| **instructions** | **String** | Custom setup instructions for the user | [optional] |
| **grants_count** | **Float** | Number of active customer grants issued from this entitlement |  |
| **products** | [**Array&lt;LinkedProductDto&gt;**](LinkedProductDto.md) | Products that are currently linked to this entitlement |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::EntitlementDetailResponseDto.new(
  id: ent_8Z1aB2cD3eF4gH5iJ6kL7m,
  business_id: bus_12345,
  name: Premium GitHub Access,
  type: GITHUB,
  status: ACTIVE,
  created_at: 2026-06-10T12:00:00.000Z,
  updated_at: 2026-06-10T12:00:00.000Z,
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
  instructions: Clone the repository and run npm install.,
  grants_count: 42,
  products: null
)
```

